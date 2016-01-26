/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

/**
 *
 * @author Prabhakaran
 */
import java.sql.*;

public class DatabaseConnectivity {
    public static void main(String[] args) {
        try {
            Class.forName("net.ucanaccess.jdbc.UcanaccessDriver");
            Connection con       = DriverManager.getConnection("jdbc:ucanaccess://C:\\Users\\Prabhakaran\\Documents\\test.accdb");
            Statement  statement = con.createStatement();
            String     qry       = "SELECT * FROM marks";
            ResultSet  rs        = statement.executeQuery(qry);

            while(rs.next()) {
                String id    = rs.getString("ID") ;
                String name = rs.getString("name");
                String mark = rs.getString("mark");
                System.out.println(name +" - "+ mark);
            }
            rs.close();
        } catch (Exception ex) {
            System.out.println(ex);
        }
    }   
}
