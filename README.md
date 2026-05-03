# DAO-e-JDBC
Banco de Dados integrado com Java. Pesquisa de JDBC e DAO.

O JDBC funciona através de drivers que são responsáveis pela conexão com o banco e execução das instruções SQL.
Baseada em drivers, para funcionar, esses drivers precisam estar carregados na memória. Quem gerencia esse carregamento é a _classe java.sql.DriverManager_: ao ser instanciado, o driver se registra nela e a partir daí já podem ser criadas conexões utilizando-o. Os métodos _registerDriver_(Driver driver) e _deregisterDriver_(Driver driver) são utilizados para registrar ou remover o registro de um driver, mas a menos que você esteja desenvolvendo seu próprio driver, não é necessário preocupar-se com esses métodos.
O javax.sql.DataSource pode ser consultado em JNDI usando jndiName definido no elemento de configuração dataSource ou cicsts_dataSource . Esse objeto javax.sql.DataSource pode ser usado para que um objeto java.sql.Connection interaja com o banco de dados.

## Diferenças entre os recursos JDBC do Liberty e o recurso CICS JDBC
LiberdadeJDBC fechará automaticamente a conexão após a conclusão do processamento, fazendo com que a transação seja revertida ou confirmada, dependendo docommitOrRollbackOnCleanup atributo dodataSource elemento. A configuração padrão érollback , então um implícitojava.sql.Connection.commit() deve ser chamado, fazendo com que oCICS unidade de trabalho a ser comprometida.

CICS JDBC é gerenciado pela unidade de trabalho CICS . As atualizações do banco de dados são confirmados ou revertidos quando a tarefa CICS é confirmada ou revertida.




https://www.alura.com.br/artigos/conhecendo-o-jdbc?srsltid=AfmBOopkKo-kgxkeLvkI-iCFSjgY0wBbRiI9FK_54SVOuvge2Oe5s1rr
https://www.devmedia.com.br/jdbc-tutorial/6638
https://www.ibm.com/docs/pt-br/cics-ts/6.x?topic=server-java-database-connectivity-jdbc
https://www.youtube.com/watch?v=sR2U6gczlsY
https://www.youtube.com/watch?v=3SrqZUB_pE4
