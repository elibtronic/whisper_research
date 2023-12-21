# whisper_research
to keep a choronicle of my work with whisper


[Working from](https://blog.castopod.org/install-whisper-cpp-on-your-mac-in-5mn-and-transcribe-all-your-podcasts-for-free/)


Trying out transcription of episode of Steering
https://github.com/BrockDSL/Steering-The-Digital-Scholarship/blob/master/Podcast-Episodes/8-STDS-Audio.mp3

`whisper_print_timings:     load time =  1700.81 ms
whisper_print_timings:     fallbacks =   0 p /   0 h
whisper_print_timings:      mel time =  4455.18 ms
whisper_print_timings:   sample time = 38458.65 ms / 83513 runs (    0.46 ms per run)
whisper_print_timings:   encode time = 1158036.75 ms /   141 runs ( 8213.03 ms per run)
whisper_print_timings:   decode time =  6981.09 ms /   153 runs (   45.63 ms per run)
whisper_print_timings:   batchd time = 1363946.38 ms / 82658 runs (   16.50 ms per run)
whisper_print_timings:   prompt time = 240912.53 ms / 31794 runs (    7.58 ms per run)
whisper_print_timings:    total time = 2815204.50 ms
./main -m models/ggml-medium.bin --output-srt -f ../audio/8-STDS-Audio.wav  14583.57s user 453.83s system 534% cpu 46:55.41 total
`
Approx 46 min to gen srt of 1:05 long audio

Transcode with ffmpeg
`ffmpge -i src.??? -ar 16000 dst.wav`

`time` - system level execution time

## how to deploy?

There is python bindings... so

- Create a notebook with anaconda local in mind
- first half installs builds tools
- lots of widgets in the interface to make it as user friendly as possible
- ffmpeg via sys to transcode as needed
- maybe ties to some cloud based storage to grab the files? / csv input

### POC

[Awesome Transcription Maker](Awesome_Transcription_Maker.ipynb) - Proof of concept notebook that will do the process top to bottom
