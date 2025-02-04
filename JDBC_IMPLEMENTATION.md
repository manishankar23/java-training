
````java
package sqldemo;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.sql.Statement;

public class main {

	public static void main(String[] args) throws ClassNotFoundException, SQLException {
		try {
		Class.forName("com.mysql.cj.jdbc.Driver");
		Connection con=DriverManager.getConnection("jdbc:mysql://localhost:3306/student","root","");
				
				Statement st=con.createStatement();
				ResultSet rs=st.executeQuery("select*from employees");
				while(rs.next()) {
					System.out.println(rs.getString(1)+""+rs.getString(2)+""+rs.getString(3)+""+rs.getString(4)+""+rs.getString(5));
				}
		}
	    
		catch(Exception e) {
		System.out.println("SUCCESSFULLY JDBC CONNECTION CREATED");
	}

}
}
````
