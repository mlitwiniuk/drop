# NAME

drop - A simple screenshot, screencast, and file upload tool with S3 support

# SYNOPSIS

drop [*options*] FILE

drop [*options*] -v

drop [*options*] -s

drop [*options*] --help


# DESCRIPTION

drop is a simple tool that allows a user to take screenshots, screencasts, and 
upload files to an external Amazon S3 bucket. Drop will always store screenshots
and screencasts locally, but will optionally upload them to Amazon S3 if configured
to do so. It also supports using custom domains.

Project home page: https://github.com/gilbertw1/drop

# OPTIONS

-a, --audio
: Enable audio recording when creating screencast

--audio-source *SOURCE*
: Audio source to use when creating screencast.  Possible values are mic or desktop
  (desktop only available on Linux)

-b, --border
: Display border around screencast area while recording (does not show in video, Linux only)

--aws-bucket *BUCKET*
: Name of S3 bucket to upload files to
  [default: empty]

--aws-key *KEY*
: Key used to authenticate with Amazon AWS
  [default: empty]

--aws-secret *SECRET*
: Secret used to authenticate with Amazon AWS
  [default: empty]

--delay *SECONDS*
: Number of seconds to dealy screenshot or screencast start.
  [default: 0]

-e, --extension *EXTENSION*
: Override extension of resulting file
  [default: empty]

-f, --filename *FILENAME*
: Override filename of resulting file
  [default: empty]

--filename-strategy *STRATEGY*
: Strategy used to rename files when uploading to Amazon S3. Valid values are exact, 
  append, replace. Exact uses the exact filename, append will append a random string 
  to the end, prepend will prepend a random string, and replace will replace the filename
  with a random string
  [default: prepend]

-h, --help
: Prints help information

--host *HOST*
: Custom host to use when generating URLs. If setting a host, S3 bucket and domain 
  should be properly configured for static hosting.

-i, --tray-icon
: Enable tray icon while recording

-k, --stop-key *KEYBDINDING*
: Keybinding used to stop recording, eg. <ctrl><alt>q (Linux only)
 [default: empty]

-m, --mouse
: Show mouse cursor in screencast.

-q, --quiet
: Do not display desktop notifications

-u, --unique-length *LENGTH*
: Length of unique string used to create filenames.
  [default 10]

-t, --transparent
: Enable transparent selection overlay, compositor is required (Linux only)

-V, --version
: Prints version information

--verbose
: Enables verbose logging

-s, --screenshot
: Capture screenshot

-v, --video
: Record video screencast

--video-format *FORMAT*
: Format to use when recording screencasts. Valid values are mp4 and gif
  [default mp4]
