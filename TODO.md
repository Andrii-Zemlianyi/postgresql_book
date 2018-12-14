Fixes:

 * https://www.citusdata.com/blog/2017/08/18/introducing-wal-g-faster-restores-for-postgres/
 * В главе "Репликация". "В частности, конфликты могут возникать по поводу того, в каком порядке должны применяться обновления. Например, предположим, что в результате выполнения транзакции А происходит вставка строки в реплику X, после чего транзакция B удаляет эту строку, а также допустим, что Y — реплика X. Если обновления распространяются на Y, но вводятся в реплику Y в обратном порядке (например, из-за разных задержек при передаче), то транзакция B не находит в Y строку, подлежащую удалению, и не выполняет своё действие, после чего транзакция А вставляет эту строку. Суммарный эффект состоит в том, что реплика Y содержит указанную строку, а реплика X — нет." Суть конфликта не понятна. Вообще непонятна.
 * В описании потоковой репликации ни слова про слоты репликации и настройку обратной связи. Это важный функционал репликации. Кстати там можно и про конфликты потоковой репликации рассказать.
 * В главе "Бэкап и восстановление PostgreSQL" Нет про горячее резервное копирование. Например, про pg_basebackup.
 * Нет ничего про настройку autovacuum. Крайне важная тема. https://www.citusdata.com/blog/2016/11/04/autovacuum-not-the-enemy/
 * В главе про dblink можно сказать, что модуль позволяет эмулировать автономные транзакции.
 * https://github.com/dhamaniasad/awesome-postgres

 * https://www.timescale.com/
 * https://www.pipelinedb.com/
 * https://github.com/powa-team/pg_qualstats/
 * https://github.com/rjuju/pg_track_settings
 * https://github.com/powa-team/pg_stat_kcache/
 * https://github.com/HypoPG/hypopg
 * https://github.com/citusdata/pg_paxos/
 * https://pgxn.org/dist/cyanaudit
 * https://github.com/pgMemento/pgMemento
 * https://pgtap.org/
