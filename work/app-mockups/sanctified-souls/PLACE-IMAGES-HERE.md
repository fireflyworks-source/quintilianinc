# Place Sanctified Souls app mockups here

HTML expects: AppMockups1.jpg through AppMockups10.jpg

Source: Sanctified souls mockups folder in your handoff archive. Source
files are named "App Mock ups1.jpg" through "App Mock ups10.jpg" (with
spaces). Strip the spaces when copying:

  for f in "App Mock ups"*.jpg; do
    cp "$f" "$(echo "$f" | tr -d ' ')"
  done
