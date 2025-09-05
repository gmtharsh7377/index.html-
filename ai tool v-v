/*
AI Video Generator — Single-file React frontend (Tailwind)

Added Feature:
- Input field for a video link (URL). Users can paste a link instead of uploading a file.
- This URL will be sent to the backend for conversion into anime/3D/cartoon styles.

Other features remain unchanged.
*/

import React, { useState, useRef } from "react";

function SEOHead() {
  React.useEffect(() => {
    document.title = "AI Video Studio — Real, 3D, Anime & Cartoon Videos";
    const metaDescription = document.createElement("meta");
    metaDescription.name = "description";
    metaDescription.content = "Create high-quality real, 3D, anime, and cartoon videos using AI-powered pipelines. Fast presets, preview, and monetizable AdSense space.";
    document.head.appendChild(metaDescription);

    const ogTitle = document.createElement("meta");
    ogTitle.setAttribute("property", "og:title");
    ogTitle.content = "AI Video Studio — Real, 3D, Anime & Cartoon Videos";
    document.head.appendChild(ogTitle);

    const ogDesc = document.createElement("meta");
    ogDesc.setAttribute("property", "og:description");
    ogDesc.content = metaDescription.content;
    document.head.appendChild(ogDesc);

    return () => {
      document.head.removeChild(metaDescription);
      document.head.removeChild(ogTitle);
      document.head.removeChild(ogDesc);
    };
  }, []);
  return null;
}

export function AdSenseConfig({ pubId = "ca-pub-REPLACE_WITH_YOURS", slotId = "REPLACE_SLOT" }) {
  React.useEffect(() => {
    if (typeof window === "undefined") return;
    if (!document.querySelector("script[data-adsense-loaded]")) {
      const s = document.createElement("script");
      s.async = true;
      s.setAttribute("data-adsense-loaded", "true");
      s.src = `https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=${pubId}`;
      s.crossOrigin = "anonymous";
      document.head.appendChild(s);
    }
  }, [pubId]);

  return (
    <div className="w-full flex justify-center my-4" aria-hidden>
      <ins className="adsbygoogle block w-full max-w-4xl h-20 md:h-60"
        style={{ display: "block" }}
        data-ad-client={pubId}
        data-ad-slot={slotId}
        data-ad-format="auto"
        data-full-width-responsive="true"></ins>
      <script>{`(adsbygoogle = window.adsbygoogle || []).push({});`}</script>
    </div>
  );
}

export default function AIVideoStudio() {
  const [style, setStyle] = useState("anime");
  const [quality, setQuality] = useState("hd");
  const [prompt, setPrompt] = useState("");
  const [file, setFile] = useState(null);
  const [videoLink, setVideoLink] = useState("");
  const [status, setStatus] = useState("idle");
  const [progress, setProgress] = useState(0);
  const [previewUrl, setPreviewUrl] = useState("");
  const [finalUrl, setFinalUrl] = useState("");
  const fileRef = useRef();

  const generate = async () => {
    if (!prompt && !file && !videoLink) {
      alert("Please provide a prompt, a reference file, or a video link.");
      return;
    }
    setStatus("queued");
    setProgress(5);

    try {
      const formData = new FormData();
      formData.append("style", style);
      formData.append("quality", quality);
      formData.append("prompt", prompt);
      if (file) formData.append("refFile", file);
      if (videoLink) formData.append("videoLink", videoLink);

      const createResp = await fetch("/api/generate", {
        method: "POST",
        body: formData,
      });

      if (!createResp.ok) throw new Error("Failed to enqueue job");
      const { jobId } = await createResp.json();

      setStatus("processing");
      setProgress(20);

      let attempts = 0;
      while (attempts < 120) {
        await new Promise((r) => setTimeout(r, 2000));
        attempts++;
        const st = await fetch(`/api/generate?jobId=${encodeURIComponent(jobId)}`);
        if (!st.ok) throw new Error("Status check failed");
        const info = await st.json();
        setProgress(info.progress ?? Math.min(95, progress + 10));
        if (info.previewUrl) setPreviewUrl(info.previewUrl);
        if (info.status === "done") {
          setFinalUrl(info.finalUrl);
          setStatus("done");
          setProgress(100);
          break;
        }
        if (info.status === "failed") {
          setStatus("failed");
          break;
        }
      }

      if (status !== "done") setStatus((s) => (s === "failed" ? s : "timed_out"));
    } catch (err) {
      console.error(err);
      setStatus("failed");
    }
  };

  const handleFile = (e) => {
    const f = e.target.files[0];
    if (f) setFile(f);
  };

  return (
    <main className="min-h-screen bg-gray-50 text-gray-900 p-4 md:p-8">
      <SEOHead />
      <header className="max-w-6xl mx-auto mb-6">
        <div className="flex items-center justify-between">
          <h1 className="text-2xl md:text-4xl font-extrabold">AI Video Studio</h1>
          <nav className="space-x-4 text-sm opacity-80">
            <a href="#features" className="hover:underline">Features</a>
            <a href="#create" className="hover:underline">Create</a>
          </nav>
        </div>
        <p className="mt-2 text-sm text-gray-600">Create realistic, 3D, anime, and cartoon videos with AI-powered presets. Ad space included for monetization.</p>
      </header>

      <section className="max-w-6xl mx-auto">
        <AdSenseConfig pubId={"ca-pub-REPLACE_WITH_YOURS"} slotId={"REPLACE_SLOT"} />
      </section>

      <section id="create" className="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-6">
        <div className="md:col-span-1 bg-white rounded-2xl p-4 shadow">
          <h2 className="font-semibold text-lg">Create new video</h2>

          <label className="block mt-4">
            <span className="text-sm">Style</span>
            <select value={style} onChange={(e) => setStyle(e.target.value)} className="mt-1 block w-full rounded-md border p-2">
              <option value="real">Real</option>
              <option value="3d">3D</option>
              <option value="anime">Anime</option>
              <option value="cartoon">Cartoon</option>
            </select>
          </label>

          <label className="block mt-4">
            <span className="text-sm">Quality</span>
            <select value={quality} onChange={(e) => setQuality(e.target.value)} className="mt-1 block w-full rounded-md border p-2">
              <option value="sd">SD (fast)</option>
              <option value="hd">HD (balanced)</option>
              <option value="4k">4K (slow)</option>
            </select>
          </label>

          <label className="block mt-4">
            <span className="text-sm">Prompt / Instructions</span>
            <textarea value={prompt} onChange={(e) => setPrompt(e.target.value)} placeholder="Describe the scene, characters, motion, tone..." className="mt-1 w-full rounded-md border p-2 h-24" />
          </label>

          <label className="block mt-4">
            <span className="text-sm">Reference file (optional)</span>
            <input ref={fileRef} type="file" accept="image/*,video/*" onChange={handleFile} className="mt-1 w-full" />
            {file && <p className="text-xs mt-1 text-gray-600">Selected: {file.name}</p>}
          </label>

          <label className="block mt-4">
            <span className="text-sm">Video link (optional)</span>
            <input type="url" placeholder="Paste video URL here" value={videoLink} onChange={(e) => setVideoLink(e.target.value)} className="mt-1 block w-full rounded-md border p-2" />
          </label>

          <div className="flex items-center gap-2 mt-4">
            <button onClick={generate} className="px-4 py-2 rounded-lg bg-indigo-600 text-white shadow hover:opacity-95">Generate</button>
            <button onClick={() => { setPrompt(""); setFile(null); setVideoLink(""); if (fileRef.current) fileRef.current.value = null; }} className="px-3 py-2 rounded-lg border">Reset</button>
          </div>

          <div className="mt-4 text-sm">
            <p>Status: <strong className="capitalize">{status}</strong></p>
            <div className="w-full bg-gray-200 rounded-full h-2 mt-2">
              <div className="h-2 rounded-full bg-indigo-500" style={{ width: `${progress}%` }} />
            </div>
          </div>
        </div>

        <div className="md:col-span-2 space-y-4">
          <div className="bg-white rounded-2xl p-4 shadow">
            <h3 className="font-semibold">Preview</h3>
            {previewUrl ? (
              <video src={previewUrl} controls className="w-full mt-3 rounded-lg" />
            ) : (
              <div className="w-full h-48 flex items-center justify-center border-2 border-dashed rounded-lg mt-3">
                <p className="text-gray-500">Preview will appear here once available</p>
              </div>
            )}

            {finalUrl && (
              <div className="mt-4">
                <h4 className="text-sm font-medium">Final video</h4>
                <video src={finalUrl} controls className="w-full mt-2 rounded-lg" />
                <a className="inline-block mt-2 text-sm underline" href={finalUrl} download>Download final video</a>
              </div>
            )}
          </div>
        </div>
      </section>
    </main>
  );
}
