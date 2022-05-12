# subject-220512

## GAS マクロをメニューから実行
```gs
// ************************************
// メニューの追加
// ************************************
function onOpen(e) {

  var ui = SpreadsheetApp.getUi();
  ui.createMenu('スクリプトの実行')
    .addItem('実行', 'myFunction')
    .addToUi();
	
}
/** @OnlyCurrentDoc */

function myFunction() {
  var spreadsheet = SpreadsheetApp.getActive();
  spreadsheet.getActiveRange().autoFill(spreadsheet.getRange('G1:G1000'), SpreadsheetApp.AutoFillSeries.ALTERNATE_SERIES);

};
```
