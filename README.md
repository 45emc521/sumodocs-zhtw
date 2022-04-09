# SUMO 說明文件

SUMO 說明文件是以 [MkDocs](https://www.mkdocs.org/) 撰成，並託管於 GitHub。

本倉儲 repository（SUMO 說明文件正體中文版）是非官方維護版本，旨在為你提供高品質的 SUMO 車流模擬軟體中文說明文件。

你可以在以下網址查看 SUMO 說明文件的中文版本：<https://sumodocs-zhtw.emc521.tw>；或者，你也可以瀏覽本文件的原文（英文）版本：<https://sumo.dlr.de/docs/>。

本讀我檔案所提及之內容大多通用於中文版及原文版網站。如有不同之處會特別以英文描述。
The content of README.md can be applied mostly on both Chinese and English Documentation websites. If there are some differences, an English description will be shown in this file.

## 入門

### 前置需求

- Python > 3.5 （*mkdocs-macros-plugin* 需要）

### 安裝到電腦上

Clone 這個 repository：

```
git clone https://github.com/eclipse/sumo.git
```

然後切換到 `sumodocs-zhtw`目錄內。

安裝 MkDocs、MkDocs 的外掛和 plantuml：

```
pip install -r requirements.txt
```

如果出現與 plantuml 相關的錯誤，請根據你的系統重新安裝 plantuml，如 Ubuntu 上的指令為 `sudo apt-get install plantuml`。

要在本機上測試網站，請輸入：

```
mkdocs serve
```

`mkdocs serve` 指令會在每次網站文件有變動時，重新建置整個網站。如果只想重新建置內容有所變動的文件，請改輸入 `mkdocs serve --dirtyreload`。[了解詳情](https://www.mkdocs.org/about/release-notes/#support-for-dirty-builds-990)。

**為了確定可以正常上線，建議你先在本機端進行測試。請在瀏覽器端輸入 127.0.0.1:8000（或你自定義的網址）以存取本機端網站。**

如果只想建置網站但不上線或在本機端測試，請輸入以下指令：

```
mkdocs build
```

這會建立一個名為 *site* 的資料夾，且含有網站需要的所有 HTML 與 CSS 檔案。

## 貢獻

如您有心，無論中文版或原文版，都歡迎您自由修改及改善 SUMO 說明文件。所有更改都須提出 pull 要求。
如您閱讀中文版網站，您可以在說明文件網站內，每頁的右上方點擊「在 GitHub 上編輯中文版」，或者直接按下快速鍵 `e` 就可以開始編輯。

If you are reading on (https://sumo.dlr.de/docs), you can click on the "Edit on GitHub" button in the top right corner of every page, or just simply press the `e` key on your keyboard.

在編輯中文版或原文版文件前，強烈建議您先閱讀 [編輯文件教學](https://sumo.dlr.de/docs/Editing_Articles.html)，將可讓您快速上手並了解如何編輯說明文件。

亦歡迎您針對文件的錯誤或錯誤給予建議。如是中文版，請到 [GitHub 的 issue 頁面](https://github.com/45EMC521/sumodocs-zhtw/issues)提出建議。

If you are using (httpd://sumo.dlr.de/docs), you can also report typos and such, opening an issue [here](https://github.com/eclipse/sumo/issues).