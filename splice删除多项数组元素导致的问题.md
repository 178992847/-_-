splice()删除数组项，会改变原数组，接着会导致 index 发生改变。所以，可以把 index 排序，由大到小，那么 splic()先删大的 index 再删小的 index，原数组就算发生改变，那也没事了。
this.saveItemIndexes
  .sort((a, b) => {
     return b - a;
    })
  .map((item) => {
    this.tableData.splice(item, 1);
    });