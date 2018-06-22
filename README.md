# learn-postgresql
## Architecuture:
* https://en.wikibooks.org/wiki/PostgreSQL/Architecture

## 事物隔离级别
* Read uncommited  
  * 我看见了将来可能不存在的事物；正在孕育的事物，但后来失败了。
* Read commited    
  * 我看得见同一个事物的其他人对它的改变；
* Repeatable read  
  * 我第一眼看见你，每次瞧你，你都是老样子； 但我能觉察到有新人来，有旧人离开。
* Serializable     
  * 我看到的世界只有我正在对他进行改造，不会有让我意外的其他变化。 
## MVCC 的好处
 * 读不阻塞写, 写不阻塞读, 并发度提高。如果不用多版本，只有一份数据，读写会有冲突，会互相阻塞。
 * 写写肯定要阻塞，写同一份数据，要有锁。和乐观锁，有所区别。
 * Postgres的事物编号的wraparound问题？如何解决:
  * https://www.slideshare.net/pgdayasia/introduction-to-vacuum-freezing-and-xid 
  * https://www.cybertec-postgresql.com/en/autovacuum-wraparound-protection-in-postgresql/#
