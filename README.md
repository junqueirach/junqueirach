# Hi, I'm Luiz Junqueira 👋

**Infrastructure & renewable energy investment professional (20+ years, PMP) who builds private, local-first AI tools.**
Zürich, Switzerland · [junqueira.ch](https://www.junqueira.ch) · [LinkedIn](https://www.linkedin.com/in/luizjunqueira/)

I have spent nearly two decades developing, financing and delivering hydropower, solar and gas assets across Latin America, Africa and Europe. Today I combine that domain knowledge with hands-on AI engineering.

## What I'm working on

**Turning expert knowledge into private AI.** Energy and infrastructure companies hold know-how and trade secrets they cannot paste into a public chatbot. I am building the pipeline to make that knowledge usable by AI *on their own infrastructure*:

`recordings / PDFs / documents / subtitles` → **clean Markdown corpus** → **AI revision, checked** ([tcqa](https://github.com/junqueirach/transcript-corpus-qa)) → **RAG** (retrieval-augmented generation) → *later:* **fine-tuning** a model on the company's own material

<p align="center"><img src="assets/pipeline.png" alt="From expert knowledge to private AI" width="900"></p>

## Projects

All tools were built with Claude (Anthropic) as coding partner. I write the requirements, test on real data and iterate. Every earlier version is kept in each repo's `archive/` folder.

| Project | What it does | Size |
|---|---|---|
| [**TranscriptLab**](https://github.com/junqueirach/transcriptlab) | Whisper transcription with checked model downloads, YouTube/podcast capture and Markdown polishing into a RAG-ready corpus. Windows .exe download in Releases, update check built in | ~34.9k lines, 77 versions |
| [**MD Converter**](https://github.com/junqueirach/md-converter) | PDF/Office/HTML/EPUB, subtitles and more to Markdown with local engines: light ones run in parallel workers, heavy ones (Docling, marker, MinerU, Surya…) in isolated environments with checked installs. Batch queue that survives a restart, quality badges, corpus export. Windows .exe download in Releases, update check built in | ~11.4k lines, 50 versions |
| [**tcqa**](https://github.com/junqueirach/transcript-corpus-qa) | AI revision of speech-to-text transcripts that can be checked: a Claude Code agent corrects a whole corpus and a second agent re-checks every correction; then an offline checker (no AI) proves each transcript changed only what its log says, before the text enters a RAG or fine-tuning corpus | Agent + checker, 14 checks, 238 tests, CI on Ubuntu and Windows |
| [**RadioSave**](https://github.com/junqueirach/radiosave) | Scheduled recorder for online radio: captures interviews and author programs unattended, as raw material for the transcript pipeline. Records every station in its own time zone, resumes dropped streams. Windows .exe download in Releases, update check built in | ~11.4k lines, 7 versions |
| [**Tiny Recorder**](https://github.com/junqueirach/tiny-recorder) | Very light meeting recorder: everything the computer plays and everything you say in one tagged MP3, with no AI and no cloud. Captures meetings and calls as raw material for the transcript pipeline. Windows .exe download in Releases | ~4.3k lines, 5 versions |
| [**SRT Studio**](https://github.com/junqueirach/srt-studio) | Subtitle translation, repair and sync with Claude (formerly SRT Translator): SRT, ASS/SSA, WebVTT and other text formats, sync to another subtitle or to the video's audio, subtitles taken from MKV/MP4, source check and repair, quality control, live pricing and cost estimates. Windows .exe download in Releases | ~9.3k lines, 14 versions |

<p align="center"><img src="assets/iterations.png" alt="Iteration history" width="700"></p>

## How I work with AI

- Write a clear brief first, then iterate in small versioned steps
- Give the AI rules it must obey (module boundaries, naming, safety checklists); [MediaClinic](https://github.com/junqueirach/mediaclinic) shows this written contract in practice
- Test on real data, log everything, fix the root cause
- Keep the history public
- Keep confidential data local and secrets out of the code

## Engineering roots

Not everything here is AI. I am a civil engineer by training, and one older project belongs on this page.

**[dlearn-ppd](https://github.com/junqueirach/dlearn-ppd)** is my 2001 civil-engineering graduation project at UNESP Bauru, rebuilt for current machines. It comes from research on dynamic structural analysis: DLEARN, the finite-element program published with T.J.R. Hughes' textbook, extended with Prof. Heitor M. Bottura's Hermitian time-integration algorithms. The pre-processor I wrote in Turbo Pascal generates DLEARN's input files from a question-and-answer dialogue. In 2026 I rebuilt DLEARN with gfortran and, with Claude, added a tested Python rewrite of the pre-processor. Checking my 2001 program against the Fortran exposed three bugs in it, documented in the repo.

## Off the clock

Two hobbies where I build for people I know: my own film library, and my mother-in-law's embroidery. They sit apart from the professional pipeline above.

### 🎬 My own media library

One of my hobbies is keeping my films and series in my own offline library: rips of the DVDs and Blu-rays I have bought, served from a home media server or NAS to **Plex, Kodi, Emby or Jellyfin**. I use the tools below every day, and they are built for people who run the same kind of library.

**Why keep your own copies?** Streaming catalogues change without asking you. Titles leave with little or no notice, sometimes in the middle of a series, and the subscription price does not go down when the catalogue shrinks. A disc on my shelf and a file on my disk are still there next year: in the quality I chose, with the audio and subtitle languages I want, with no account, no licence server and no internet connection needed.

The catch is that a big library only works if it is tidy. Missing artwork, wrong IDs, broken metadata files and inconsistent genres make **Plex, Kodi, Emby or Jellyfin** show the wrong movie, or none at all. These tools keep it healthy:

| Tool | What it does |
|---|---|
| [**MediaClinic**](https://github.com/junqueirach/mediaclinic) | For **Plex, Kodi, Emby and Jellyfin users**: scans a movie library, shows every metadata, artwork and video problem in one colour-coded table and fixes the common ones safely. You tick the programs that play your movies (Kodi, Plex, Jellyfin, Emby, Infuse, old Windows media centers): the checks and the file names a fix writes follow what each one really reads, tested on real servers and an Apple TV. Latest release: **v0.20.2**: rename movie folders from a pattern (with Undo), age ratings for your countries, the movies missing from each collection, a set.nfo editor, and a movie counts as OK when it has audio or subtitles in one of your languages. [Windows .exe download](https://github.com/junqueirach/mediaclinic/releases/latest) |
| [**Kodi Files Generator**](https://github.com/junqueirach/kodi-files-generator) | For **Kodi, Jellyfin and Emby users**: opens a TV series folder, takes the episode data from your own CSV or Excel list or from free sources (TheTVDB pages, TVmaze), and writes every episode and series NFO, XML and image after a preview, with backup and undo. Windows .exe download in Releases |

Subtitles are part of the same job: I use [**SRT Studio**](https://github.com/junqueirach/srt-studio) (formerly SRT Translator, listed under AI projects above) to translate, repair and sync the subtitles of the films I own; [MD Converter](https://github.com/junqueirach/md-converter) turns subtitle files into Markdown for my transcript corpus.

<p align="center"><img src="https://github.com/junqueirach/mediaclinic/raw/main/docs/screenshots/mediaclinic.png" alt="MediaClinic" width="800"></p>

*This is about keeping what I have bought, not about piracy. Rules on copying discs differ by country, so check yours.*

### 🧵 Embroidery: tools for my mother-in-law

My mother-in-law embroiders a lot, and I watch the same difficulties come back: it is hard to see how a design will actually be stitched before the machine runs, and turning a picture into a file the machine can read takes many manual steps. I build these two tools from those difficulties, with her as the first tester. Both are **private for now**: there is no public download, and they are still in testing.

| Tool | What it does |
|---|---|
| **PES Viewer** | A light Windows viewer that opens PES and about 40 other embroidery formats and shows how the design is stitched: every stitch, colour, trim and jump, the stitching order and the measured density. It only views; it never changes a file. |
| **PES Generator** | Turns an image into embroidery files in several sizes, as PES or other machine formats, with a check of each file and a sheet per size. The automatic stitching works best for flat-colour drawings and logos and is weaker for photos, so a test stitch on scrap fabric is always advised. |

## Tech

Python · Tkinter · WASAPI audio capture · Whisper · MarkItDown · Docling · ffmpeg · yt-dlp · pysubs2 · Claude API · Claude Code agents · Markdown pipelines · RAG concepts · Kodi/Plex NFO and XML metadata · pytest · GitHub Actions CI · PyInstaller and Nuitka Windows builds

## Get in touch

Open to senior roles in infrastructure and renewables, and to conversations about private AI for energy companies.
📧 junqueira.ch@gmail.com · 🌐 [junqueira.ch](https://www.junqueira.ch)
