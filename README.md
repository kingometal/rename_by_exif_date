# rename_by_exif_date
This script takes a list of files as arguments and appends a prefix to the filename, which contains the date and time from the exif data

The prefix format is YYYYMMDD-hhmmss_

## Usage
usage: ./rename_by_exif_date [Options] Filename1 Filename2 Filename3...

Options:

  -d or --dry-run

    -d 1 enables dry run, which means, no data is actully written, and no files are renamed

    -d 0 disables dry run. This option is needed to actually rename files.

    default is -d 1

  -s

    silent mode: no user confirmations are required

  -se or --show-errors

    -se 0 disables messages when a file can not be renamed. Default is 1

  -ss or --show-skipped

    -ss 0 disables messages when a file was not renamed because it was skipped. A file is usually skipped if it already has the date-time-prefix, or it contains exif data which is full of zeroes, meaning the date and time were not set on the camera

## Important:
Dry run is enabled by default. You have to run it with -d 0 to make actual changes on you files
