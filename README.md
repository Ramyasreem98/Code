Home.jsp

<%@ page language="java" contentType="text/html; charset=ISO-8859-1"
    pageEncoding="ISO-8859-1"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
<title>HospitalInformationSystems</title>
</head>
<body background="images/bc1.jpg">
<br/><br/><br/>
<br/><br/><br/> 
 <center>
          <a href="Home.jsp"><span>Home Page</span></a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          <a href="PatientLogin.jsp"><span>Patient</span></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
           <a href="AdminLogin.jsp"><span>Admin</span></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
           <a href="HospitalStaff.jsp"><span>Hospital Staff</span></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   
         </center>
<br/>
</body>
</html>


AdminLogin.jsp
<%@ page language="java" contentType="text/html; charset=ISO-8859-1"
    pageEncoding="ISO-8859-1"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
<title>HospitalInformationSystems</title>
</head>
<body background="images/bc1.jpg">
<br/><br/><br/><br/><br/><br/>
  <center>

          <a href="Home.jsp"><span>Home Page</span></a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          <a href="PatientLogin.jsp"><span>Patient</span></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
           <a href="AdminLogin.jsp"><span>Admin</span></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
           <a href="HospitalStaff.jsp"><span>Hospital Staff</span></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

           </center>
               <br/><br/><br/>
        <center><p> <h1 style="font: normal;"><span>Admin Login</span></h1> </p></center>
      <br/>
      <center>       <p>
            <form action="AdminLogin" method="post">
            <table>
            
             <tr><td>Admin Name</td><td>:</td><td><input type="text" name="aname"></input></td></tr>
              <tr></tr>

               <tr><td>Password</td><td>:</td><td><input type="password" name="pwd"></input></td></tr>
              <tr></tr>

              <tr><td></td><td></td><td><input type="submit" name="go" value="LOGIN"></input><input type="reset" ue="RESET"></input></td></tr>
            </table>           
 <br/>         
            </form>             
  </center><br/>
</body>
</html>


AdminLogin.java
package com.Admin;
import java.io.IOException;
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import com.Bean.AdminBean;
import com.Implementations.Implementation;
import com.Interfaces.PatientInterface;
/** * Servlet implementation class AdminLogin */
@WebServlet("/AdminLogin")
public class AdminLogin extends HttpServlet {
	private static final long serialVersionUID = 1L;       
    /*** @see HttpServlet#HttpServlet()    */
    public AdminLogin() {
        super();
        // TODO Auto-generated constructor stub
    }/*** @see HttpServlet#doGet(HttpServletRequest request, HttpServletResponse response) */	
protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
// TODO Auto-generated method stub
} /*** @see HttpServlet#doPost(HttpServletRequest request, HttpServletResponse response) */
protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {	
// TODO Auto-generated method stub
	String name=request.getParameter("aname");
		String pwd=request.getParameter("pwd");		
		System.out.println("Admin Login...........");		
		if(name.equals("admin") && pwd.equals("admin")){		 	response.sendRedirect("AdminHome.jsp");
	}	
else{	

	}	
	}
}


AdminHome.jsp
<%@ page language="java" contentType="text/html; charset=ISO-8859-1"
    pageEncoding="ISO-8859-1"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">

<title>HospitalInformationSystems</title>
</head>

<body background="images/bc1.jpg">
<br/><br/><br/><br/><br/><br/>
 
 <center>
          <a href="AdminHome.jsp"><span>Home Page</span></a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

          <a href="AddHospitalSaffDetails.jsp"><span>Add HospitalSaff</span></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          <a href="PatientDetails4.jsp"><span>Patient Details</span></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

          <a href="HospitalSatffDetails.jsp"><span>HospitalSaff Details</span></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;         

          <a href="AdminLogin.jsp"><span>Logout</span></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        
           </center>
               <br/><br/><br/>
        <center>
<p> <h1 style="font: normal;"><span>Welcome To Admin Page</span></h1> </p></center>
      <br/><br/>

</body>
</html>


AddHospitalSaffDetails.jsp
<%@ page language="java" contentType="text/html; charset=ISO-8859-1"
    pageEncoding="ISO-8859-1"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<%@ page import="java.util.*" %>
<%@ page import="java.io.*" %>
<%@ page import="java.util.Random" %>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
<title>HospitalInformationSystems</title>
</head>
<body background="images/bc1.jpg">
<br/><br/><br/><br/><br/><br/>  <center>
          <a href="AdminHome.jsp"><span>Home Page</span></a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="AddHospitalSaffDetails.jsp"><span>Add</span></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
 <a href="AdminLogin.jsp"><span>Logout</span></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                   </center>
               <br/><br/><br/>
        <center><p> <h1 style="font: normal;"><span>Add All Hospital Staff Details</span></h1> </p></center>
      <br/>      <center>       <p>
            <form action="HospitalStaffRegister" method="post">
            <table>
            <tr><td>Name</td><td>:</td><td><input type="text" name="name" ></input></td></tr>
            <tr></tr>
             <tr><td>Password</td><td>:</td><td><input type="Password" name="pwd"></input></td></tr>
              <tr></tr>
               <tr><td>Qualification</td><td>:</td><td><input type="text" name="qualification"></input></td></tr>
                <tr></tr>
                     <tr><td>Role </td><td>:</td><td> <select id="id" name="role" >
                    <option value="0">--select--</option>
                    <option value="Nurse">Nurse</option>
                    <option value="MedicalTechnician">MedicalTechnician</option>
                    <option value="Doctor">Doctor</option>
                    <option value="AdministrationStaff">AdministrationStaff</option>
                  </select><br></br></td></tr>                
   <tr><td>Email</td><td>:</td><td><input type="email" name="email"></input></td></tr>               <tr></tr>
               <tr><td>Address</td><td>:</td><td><input type="text" name="address"></input></td></tr>
              <tr></tr>
              <tr><td>Key</td><td>:</td><td><input type="text" name="key" value="<%=(int)(Math.random()*10009)%>"></input></td></tr> 
              <tr></tr>
              <tr><td></td><td></td><td><input type="submit" name="go" value="Register"></input><input type="reset"  value="RESET"></input></td></tr>
            </table>            
            </form>              
   </center><br/>
</body>
</html>


HospitalStaffRegister.java
package com.Admin;
import java.io.IOException;
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import javax.servlet.http.HttpSession;
import org.eclipse.jdt.internal.compiler.lookup.ImplicitNullAnnotationVerifier;
import com.Bean.AdminBean;
import com.Bean.PatientBean;
import com.Interfaces.PatientInterface;
import com.Implementations.Implementation;
/*** Servlet implementation class NurseRegister*/
@WebServlet("/HospitalStaffRegister")
public class HospitalStaffRegister extends HttpServlet {
	private static final long serialVersionUID = 1L;
           /*** @see HttpServlet#HttpServlet()*/
    public HospitalStaffRegister() {
        super();
        // TODO Auto-generated constructor stub
    }	
/*** @see HttpServlet#doGet(HttpServletRequest request, HttpServletResponse response) */
	protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		// TODO Auto-generated method stub
	}
	/*** @see HttpServlet#doPost(HttpServletRequest request, HttpServletResponse response) */
	protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		// TODO Auto-generated method stub
		String name =request.getParameter("name");
		String pwd =request.getParameter("pwd");
		String qualification =request.getParameter("qualification");
		String role =request.getParameter("role");
		String email =request.getParameter("email");
		String address =request.getParameter("address");
		String key =request.getParameter("key");		
		System.out.println("HospitalStaffRegister Register Page..........");
		AdminBean bean=new AdminBean();		
		bean.setName(name);
		bean.setPwd(pwd);
		bean.setQualification(qualification);
		bean.setRole(role);
		bean.setEmail(email);
		bean.setAddress(address);
		bean.setKey(key);
		System.out.println("this is nice page.........."+key);		
		PatientInterface pi=new Implementation();
		int status=pi.hospitalStaffRegister(bean);
		HttpSession session1=request.getSession();  
		session1.setAttribute("name",name);  
		session1.setAttribute("key",key); 		
	if(status==0)
	{		response.sendRedirect("AddHospitalSaffDetails.jsp");
	}	else
	{
		response.sendRedirect("Success.jsp");
	}	}
}


AdministrationStaffUpdate.java
package com.Admin;
import java.io.IOException;
import java.io.PrintWriter;
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.Statement;
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import com.Bean.PatientBean;
import com.Connections.Connections;
import com.Implementations.Implementation;
import com.Interfaces.PatientInterface;
import java.sql.*;
/*** Servlet implementation class DoctorUpdate*/
@WebServlet("/AdministrationStaffUpdate")
public class AdministrationStaffUpdate extends HttpServlet {	
	private static final long serialVersionUID = 1L;
    /*** @see HttpServlet#HttpServlet() */
    public AdministrationStaffUpdate() {
        super();
        // TODO Auto-generated constructor stub
    }	/*** @see HttpServlet#doGet(HttpServletRequest request, HttpServletResponse response) */
protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
// TODO Auto-generated method stub
	}
/*** @see HttpServlet#doPost(HttpServletRequest request, HttpServletResponse response)*/
	protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		response.setContentType("text/html;charset=UTF-8");
        PrintWriter out = response.getWriter();
		// TODO Auto-generated method stub		
		String id=request.getParameter("id");
		String name=request.getParameter("name");
		String pwd=request.getParameter("pwd");
		String problem=request.getParameter("problem");
		String problemDesc=request.getParameter("problemDesc");
		String dob=request.getParameter("dob");
		String mobile=request.getParameter("mobile");
		String gender=request.getParameter("gender");
		String mail=request.getParameter("mail");
		String address=request.getParameter("address");
		String joiningdate=request.getParameter("joiningdate");
		/*String doctorTreatmentDate=request.getParameter("doctorTreatmentDate");	
		String lastDressingDate=request.getParameter("lastDressingDate");
		String testsConductedDate=request.getParameter("testsConductedDate");*/
		String billGenerated=request.getParameter("billGenerated");		
		System.out.println("Nurse Updated Details....");
		PatientBean bean=new PatientBean();		
		bean.setId(id);
		bean.setName(name);
		bean.setPwd(pwd);
		bean.setProblem(problem);
		bean.setProblemDesc(problemDesc);
		bean.setDob(dob);
		bean.setMobile(mobile);
		bean.setGender(gender);
		bean.setMail(mail);
		bean.setAddress(address);
		bean.setJoiningdate(joiningdate);
		/*bean.setDoctorTreatmentDate(doctorTreatmentDate);
		bean.setLastDressingDate(lastDressingDate);
		bean.setTestsConductedDate(testsConductedDate);*/
		bean.setBillGenerated(billGenerated);
		try{
		Class.forName("com.mysql.jdbc.Driver");
Connectionconnection=DriverManager.getConnection("jdbc:mysql://localhost:3306/VTJDM12-2017", "root", "root");		
		Connection con=Connections.con();
        Statement st=con.createStatement();
//int i=st.executeUpdate("update patientregister SET lastDressingDate='"+lastDressingDate+"',testsConductedDate='"+testsConductedDate+"',billGenerated='"+testsConductedDate+"' where id='"+id+"'");     
        int i=st.executeUpdate("update patientregister SET billGenerated='"+billGenerated+"' where id='"+id+"'");        if(i!=0){
        response.sendRedirect("AdministrationStaffUpdateSuccess.jsp");
   }    else{
      out.println("error while updating");
     }		}		
     catch(Exception e){
         out.println(e);   
}
}
}


PatientRegister.jsp

<%@page import="com.Patient.MouseListenerExample"%>
<%@page import="java.awt.*" %>
<%@page import="java.awt.event.*" %>
<%@ page language="java" contentType="text/html; charset=ISO-8859-1"
    pageEncoding="ISO-8859-1"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
<title>Doctor Update Patient Details Page</title>
</head>
<body background="images/pbc1.jpg">
<br/><br/><br/><br/><br/><br/><br/><br/>
 
 <center>
         <a href="Home.jsp"><span>Home Page</span></a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
           <a href="PatientDetails.jsp"><span>PatientDetails</span></a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        
  <p> <h1><span>Patient Registration Form</span></h1> </p></center>
      <center>  <p>   <form action="PatientRegister" method="post"  name="s" onsubmit="return valid()">
            <table>
           
             <tr><td>Patient Name</td><td>:</td><td><input type="text"" name="name"/></td>
             <td>Patient Password</td><td>:</td><td><input type="password" name="pwd"/></td></tr>
             <tr><td>Problem</td><td>:</td><td><input type="text" name="problem"/></td>
             <td>Problem Desc</td><td>:</td><td><input type="text" name="problemDesc"/></td></tr>
             <tr><td>Date Of Birth</td><td>:</td><td><input type="text" name="dob"/></td>
             <td>Mobile</td><td>:</td><td><input type="number" name="mobile"/></td></tr>
            <tr><td>Gender</td><td>:</td><td><input type="radio" name="gender" value="Male"/>Male<input type="radio" name="gender" value="Female"/>Female</td>
             <td>Mail ID</td><td>:</td><td><input type="email" name="mail"/></td></tr>
             <tr><td>Address</td><td>:</td><td><textarea type="text" name="address" rows="4" ></textarea></td>
             <td>Joining Date</td><td>:</td><td><input type="text" name="joiningdate" value="no" readonly="readonly" /></td></tr>
             <tr><td>Doctor Treatment Date</td><td>:</td><td><input type="text" name="doctorTreatmentDate" value="no" readonly="readonly" /></td>
             <td>Discharge Date</td><td>:</td><td><input type="text" name="dischargeDate" value="no" readonly="readonly" /></td></tr>
             <tr><td>Last Dressing Date</td><td>:</td><td><input type="text" name="lastDressingDate" value="no" readonly="readonly"/></td>
             <td>Different Types of Tests </td><td>:</td><td><input type="text" name="tests" value="no" readonly="readonly"/></td></tr>
             <tr><td>Tests Conducted Date</td><td>:</td><td><input type="text" name="testsConductedDate" value="no" readonly="readonly"/></td>
             <td>Completed Bill (Till Date)</td><td>:</td><td><input type="text" name="billGenerated" value="no" readonly="readonly"/></td></tr>
             <tr><td></td><td></td><td><input type="submit" name="go" value="REGISTER"></input><input type="reset"  value="RESET"></input></td></tr>

            </table>
            </form>
            </center>
<br/><br/><br/><br/>
       
  </center><br/>
  &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; <a href="PatientDetails.jsp">Back</a>

</body>
</html>


PatientRegister.java

package com.Patient;
import java.io.IOException;
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import com.Bean.PatientBean;
import com.Implementations.Implementation;
import com.Interfaces.PatientInterface;

@WebServlet("/PatientRegister")
public class PatientRegister extends HttpServlet {
	private static final long serialVersionUID = 1L;     
    public PatientRegister() {
        super();
  	protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {		
	}	
	protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		// TODO Auto-generated method stub		
		String name=request.getParameter("name");
		String pwd=request.getParameter("pwd");
		String problem=request.getParameter("problem");
		String problemDesc=request.getParameter("problemDesc");
		String dob=request.getParameter("dob");
		String mobile=request.getParameter("mobile");
		String gender=request.getParameter("gender");
		String mail=request.getParameter("mail");
		String address=request.getParameter("address");
		String joiningdate=request.getParameter("joiningdate");
		String doctorTreatmentDate=request.getParameter("doctorTreatmentDate");
		String dischargeDate=request.getParameter("dischargeDate");		
		String lastDressingDate=request.getParameter("lastDressingDate");
		String tests=request.getParameter("tests");
		String testsConductedDate=request.getParameter("testsConductedDate");
		String billGenerated=request.getParameter("billGenerated");		
		System.out.println("Patient Registration....");
		PatientBean bean=new PatientBean();		
		bean.setName(name);
		bean.setPwd(pwd);
		bean.setProblem(problem);
		bean.setProblemDesc(problemDesc);
		bean.setDob(dob);
		bean.setMobile(mobile);
		bean.setGender(gender);
		bean.setMail(mail);
		bean.setAddress(address);
		bean.setJoiningdate(joiningdate);
		bean.setDoctorTreatmentDate(doctorTreatmentDate);
		bean.setDischargeDate(dischargeDate);
		bean.setLastDressingDate(lastDressingDate);
		bean.setTests(tests);
		bean.setTestsConductedDate(testsConductedDate);
		bean.setBillGenerated(billGenerated);		
		PatientInterface pi=new Implementation();
		int status=pi.register(bean);		
		if(status==1)
		{	response.sendRedirect("PatientLogin.jsp");
		}else
		{
		}
	} }


