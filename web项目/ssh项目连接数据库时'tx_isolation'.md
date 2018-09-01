### ssh项目连接mysql数据库出现Unknown system variable 'tx_isolation'
##### 错误
```
java.sql.SQLException: Unknown system variable 'tx_isolation'
	at com.mysql.jdbc.SQLError.createSQLException(SQLError.java:1072)
	at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3563)
	at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3495)
	at com.mysql.jdbc.MysqlIO.sendCommand(MysqlIO.java:1959)
	at com.mysql.jdbc.MysqlIO.sqlQueryDirect(MysqlIO.java:2113)
	at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2687)
	at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2616)
	at com.mysql.jdbc.StatementImpl.executeQuery(StatementImpl.java:1464)
	at com.mysql.jdbc.ConnectionImpl.getTransactionIsolation(ConnectionImpl.java:3259)
	at com.mchange.v2.c3p0.impl.NewPooledConnection.<init>(NewPooledConnection.java:120)
	at com.mchange.v2.c3p0.WrapperConnectionPoolDataSource.getPooledConnection(WrapperConnectionPoolDataSource.java:240)
	at com.mchange.v2.c3p0.WrapperConnectionPoolDataSource.getPooledConnection(WrapperConnectionPoolDataSource.java:206)
	at com.mchange.v2.c3p0.impl.C3P0PooledConnectionPool$1PooledConnectionResourcePoolManager.acquireResource(C3P0PooledConnectionPool.java:203)
	at com.mchange.v2.resourcepool.BasicResourcePool.doAcquire(BasicResourcePool.java:1138)
	at com.mchange.v2.resourcepool.BasicResourcePool.doAcquireAndDecrementPendingAcquiresWithinLockOnSuccess(BasicResourcePool.java:1125)
	at com.mchange.v2.resourcepool.BasicResourcePool.access$700(BasicResourcePool.java:44)
	at com.mchange.v2.resourcepool.BasicResourcePool$ScatteredAcquireTask.run(BasicResourcePool.java:1870)
	at com.mchange.v2.async.ThreadPoolAsynchronousRunner$PoolThread.run(ThreadPoolAsynchronousRunner.java:696)
```
#### 原因
数据库驱动jdbc版本太低。
