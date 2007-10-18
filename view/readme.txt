
http://dbflute.sandbox.seasar.org/view/general_view/index.html?goto=1:3

http://dbflute.sandbox.seasar.org/view/role_of_dbflute/index.html?goto=1




Behaviorの主なMethod ※本(BOOK)というTableを例に

============================================================ 一件検索
- - - - - - - - - - - - - - - - - - - - - - 
Book selectEntity(BookCB cb);

  指定された条件に合致する一件検索。
  検索結果が複数件の場合は例外が発生する。
  検索結果が０件の場合はnullが戻される。

- - - - - - - - - - - - - - - - - - - - - - 
Book selectEntityWithDeletedCheck(BookCB cb);

  nullが戻されないことを保証するselectEntity。
  検索結果が０件の場合は例外が発生する。

- - - - - - - - - - - - - - - - - - - - - - 
Book selectByPKValueWithDeletedCheck(Integer bookId);

  PrimaryKeyを引数にしたselectEntityWithDeletedCheck。


============================================================ リスト検索
- - - - - - - - - - - - - - - - - - - - - - 
ListResultBean<Book> selectList(BookCB cb);

  指定された条件に合致する一覧検索。
  戻り値のListResultBeanはjava.util.Listの実装Class。

- - - - - - - - - - - - - - - - - - - - - - 
PagingResultBean<Book> selectPage(BookCB cb);

  指定された条件に合致するPaging検索。
  戻り値のPagingResultBeanはjava.util.Listの実装Classであり、
  Paging処理に必要な様々な結果情報を保持している。


============================================================ １件更新
- - - - - - - - - - - - - - - - - - - - - - 
void insert(Book book);

  指定されたEntityをInsert。


- - - - - - - - - - - - - - - - - - - - - - 
PagingResultBean<Book> selectPage(BookCB cb);

  指定された条件に合致するPaging検索。
  戻り値のPagingResultBeanはjava.util.Listの実装Classであり、
  Paging処理に必要な様々な結果情報を保持している。





Book selectEntity(BookCB cb);

  指定された条件に合致する一件検索。

