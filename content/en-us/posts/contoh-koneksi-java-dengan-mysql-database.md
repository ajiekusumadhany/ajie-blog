---
title: 'Contoh Koneksi Java dengan Mysql Database'
date: Fri, 14 Jul 2023 16:42:24 +0000
draft: false
tags: ['Java', 'Pemrograman']
---

Source Code
-----------

Contoh kode program koneksi java ke database mysql:

```
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;
import java.sql.Statement;
import java.util.logging.Level;
import java.util.logging.Logger;
import javax.swing.JOptionPane;

public class KoneksiDb {
   public static Connection conn;
   public static Statement stm;
   public String usr;

    public KoneksiDb(String usr) {
       try {
           conn=DriverManager.getConnection("jdbc:mysql://192.168.10.253/a112113379",
                    "a112113379","polke001");
           stm=conn.createStatement();
           JOptionPane.showMessageDialog(null, 
                   "Koneksi Berhasil !");
       } catch (SQLException ex) {
           Logger.getLogger(KoneksiDb.class.getName()).log(Level.SEVERE, null, ex);
       }
    }

    public static Connection getConn() {
        return conn;
    }
   
    public static void main(String\[\] args) {
        KoneksiDb konn=new KoneksiDb("a112113379");
    }
 
}
```

Menambah Libraries
------------------

[![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhFXtkGKJDwRfBkvVoAofA8K4v6Gmpl_23WDnxJnlosg1H2FyUssAwcti37MJ2yRMAC6M1aVDuuTFNvQ42ldiPgykNfFDzRjuX3mZVCY74a9p2aAlbOQDmMjWtqLVcudHXupGwm36qytnAg7fd_dUJ2pOE7613AUka-xhFSzJVYvJhrKGlXBWbTxZ2reQ/s1600/Screenshot%20%2813%29.png)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhFXtkGKJDwRfBkvVoAofA8K4v6Gmpl_23WDnxJnlosg1H2FyUssAwcti37MJ2yRMAC6M1aVDuuTFNvQ42ldiPgykNfFDzRjuX3mZVCY74a9p2aAlbOQDmMjWtqLVcudHXupGwm36qytnAg7fd_dUJ2pOE7613AUka-xhFSzJVYvJhrKGlXBWbTxZ2reQ/s1600/Screenshot%20%2813%29.png)

Klik kanan Libraries lalu pilih add JAR/Folder, setelah itu pilih atau tambahkan mysql-connector-j-8.0.32

[![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg8b8s7ZDbBFe0tqdxKQHA0M7VR461SCCFjcxBsCqXSNMCxqWNZlJI_tbcwAdlmcB3uMzcTAtDYcg1y8gXZTa8J5jJvh8Y3zUDm6K86YKsadEukn6ws8BUgFiEhZhtIXXDHqnpsdbyLYDNSSUQ0Xeld56vU2ix1dclRVtPa3uENXU9qEEm9vYmDi24-1A/s1600/Screenshot%20%2814%29.png)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg8b8s7ZDbBFe0tqdxKQHA0M7VR461SCCFjcxBsCqXSNMCxqWNZlJI_tbcwAdlmcB3uMzcTAtDYcg1y8gXZTa8J5jJvh8Y3zUDm6K86YKsadEukn6ws8BUgFiEhZhtIXXDHqnpsdbyLYDNSSUQ0Xeld56vU2ix1dclRVtPa3uENXU9qEEm9vYmDi24-1A/s1600/Screenshot%20%2814%29.png)

File mysql-connector-j-8.0.32 bisa kalian unduh melalui link di bawah:

[MySql JDBC Driver](https://dbschema.com/jdbc-driver/MySql.html)