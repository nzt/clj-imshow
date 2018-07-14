# clj-imshow

[![Clojars Project](https://img.shields.io/clojars/v/clj-imshow.svg)](https://clojars.org/clj-imshow)

A implementation of OpenCV's imshow. We supports only JavaCV and JavaCPP Presets. In 2018 `imshow` and `waitKey` doesn't work on macOS, you can use this wrapper.

## Usage

```clojure
(import [org.bytedeco.javacpp.opencv_imgcodecs])
(require '[clj-imshow.core :as cvx])

(cvx/imshow "lena" (opencv_imgcodecs/imread "lena.png"))
(cvx/imshow (opencv_imgcodecs/imread "lena.png")) ;; When you give no title, title is "Untitled"
```

## License

Copyright © 2018 TANIGUCHI Masaya

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.