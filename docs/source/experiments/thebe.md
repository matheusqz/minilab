# TheBe

ThebeLab [GitHub](https://github.com/executablebooks/thebe) repository.

ThebeLab [Docs](https://thebe.readthedocs.io).

```bash
# Local Server.
jupyter notebook --port 8888 --NotebookApp.token=test-secret --NotebookApp.allow_origin='https://thebe.readthedocs.io'
open https://thebe.readthedocs.io/en/latest/_static/local.html
```

```bash
jupyter notebook --port 8888 --NotebookApp.token=test-secret --NotebookApp.allow_origin='file://'
```

```html
<html>
<head>
  <meta HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=UTF-8">
  <title>ThebeLab examples</title>
  <link rel="stylesheet" type="text/css" href="index.css" />

  <!-- Configure and load Thebe !-->
  <script type="text/x-thebe-config">
    {
      bootstrap: true,
      kernelOptions: {
        name: "python3",
        serverSettings: {
          "baseUrl": "http://127.0.0.1:8888",
          "token": "test-secret"
        }
      },
    }
  </script>
  <script type="text/javascript" src="https://unpkg.com/thebelab@^0.4.0" ></script>
  <!-- <script type="text/javascript" src="../lib/index.js"></script> -->
  <!-- load a local thebe: -->

</head>
<body>
  <h1>ThebeLab: using a local server</h1>

  <p>This page illustrates how to setup ThebeLab, using a local
  Jupyter server as kernel provider. This assumes that you have
  started the local server as:
  <pre>
    jupyter notebook --NotebookApp.token=test-secret --NotebookApp.allow_origin='<span id="origin">*</span>'
  </pre>
  and that it's running on port 8888</p>

  See also the
  <a href="https://github.com/minrk/thebelab/blob/master/examples/local.html">source file</a>.

  <pre data-executable="true" data-language="python">print("Hello!")</pre>
  <pre data-executable="true" data-language="python">1+1</pre>
  <pre data-executable="true" data-language="python">
from IPython.display import Math
Math('\sqrt{1-x^2}')
  </pre>

<script type="text/javascript">
  document.getElementById('origin').innerHTML = location.origin;
</script>
</body>
</html>
```