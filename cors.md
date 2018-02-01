### 在 flask 中处理跨域问题
```
//安装 flask-cors
pip3 install -U flask-cors

//在代码中引入
from flask_cors import CORS

app = Flask(__name__)
CORS(app)
```
