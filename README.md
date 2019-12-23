# FileSizeSurvey_TwoFileVer

## 概要

1. 環境

    - OS：Windows10 ver1909
    - RPAツール：UiPath Studio(2019.10.2)
    - Officeツール：Office365

## 初期設定

1. ./data/configを編集する

    - InputMode
        ファイルの指定方法を設定する
        Config：Configにて指定(後述のInputData_Path、OutputData_Pathを参照する)
        Input：Inputファイルをユーザ指定(Outputファイルは同一フォルダ内に作成)
        InOut：InputおよびOutputファイルをユーザ指定(Outputファイルは作成済みであること)
    - InputData_Path
        入力ファイルのフルパス
    - OutputData_Path
        出力ファイルのフルパス
    - InputData_SheetName
        処理対象のシート名

2. 入力ファイルの形式

    - Excelファイル(xlsxまたはxls)
    - ヘッダーは必須
    - 列項目
        Path：調査対象フォルダのフルパス(必須項目)
    - シート名はConfigで設定した名前であること

3. 出力ファイルの形式

    - Excelファイル(xlsx)
    - 作業日付(yyyyMMdd)のシート名に対して出力する
    - シートが存在しない場合は新規作成、存在する場合は上書き更新を行う
    - 列項目
        Path：調査対象フォルダのフルパス
        Size：ディスク上のサイズ(単位はByte)

4. エクスプローラについて
    - エクスプローラ上の「プロパティ」ボタンを使用するため、リボンメニューが表示される設定にする
