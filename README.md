# sight-dotty ![Scala CI](https://github.com/ashwinbhaskar/sight-dotty/workflows/Scala%20CI/badge.svg)
Dotty client library for Sight APIs. For details please have a look at the official [clojure library](https://github.com/siftrics/sight-clojure)

# Usage

```
import sight.client.SightClient
import sight.types.APIKey
import sight.models.{Error, Pages}

val apiKey: Either[Error, APIKey] = APIKey("xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
val files: Seq[String] = Seq("/user/john.doe/foo.pdf","/user/john.doe/baz/bmp")
val result: Either[Error, Pages] = apiKey.flatMap(key => SightClient(key).recognize(files))

```
