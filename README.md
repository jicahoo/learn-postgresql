# learn-postgresql
## Architecuture:
* https://en.wikibooks.org/wiki/PostgreSQL/Architecture

## 事物隔离级别
* Read uncommited  我看见了将来可能不存在的事物；
* Read commited    我看得见同一个事物的其他人对它的改变；
* Repeatable read  我第一眼看见你，每次瞧你，你都是老样子； 但我能觉察到有新人来，有旧人离开。
* Serializable     我看到的世界只有我正在对他进行改造，不会有让我意外的其他变化。 
