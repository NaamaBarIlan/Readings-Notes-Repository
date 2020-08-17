# SendGrid : Sending Emails

### Reading List:

##### [SendGrid Tutorial](https://docs.microsoft.com/en-us/azure/sendgrid-dotnet-how-to-send-email)
##### [SendGrid csharp](https://github.com/sendgrid/sendgrid-csharp)

---

### SendGrid Email Service Overview

SendGrid is a cloud-based email service that provides reliable transactional email delivery, scalability, and real-time analytics along with flexible APIs that make custom integration easy.

#### How to Send Email Using SendGrid with Azure

* Create a SendGrid account via the Azure Portal 

* Find your SendGrid API key:
	* Manage => Settings => API Key => Create API Key => Provide the Name of Key and set access to Mail Send => Save
	* **Important!** make sure the safely save the displayed API key. You will not have access to it again. 

* Install the SendGrid NuGet Package:
	* SendGrid's .NET class library is called **SendGrid**. It contains the following namespaces:
		* **SendGrid** for communicating with SendGrid's API.
		* **SendGrid.Helpers.Mail** for helper methods to easily create SendGridMessage objects that specify how to send emails.

* Add the below namespace declarations to the top of any C# file in which you want to access the SendGrid service:
	 ```using SendGrid;```
	 ```using SendGrid.Helpers.Mail;```

* Create an email:
	* Create a SendGridMessage object
	* Set the properties and method of the object, such as:  email sender, the email recipient, and the subject and body of the email. For example: 
		```
		var msg = new SendGridMessage();

		msg.SetFrom(new EmailAddress("dx@example.com", "SendGrid DX Team"));

		var recipients = new List<EmailAddress>
		{
			new EmailAddress("jeff@example.com", "Jeff Smith"),
			new EmailAddress("anna@example.com", "Anna Lidman"),
			new EmailAddress("peter@example.com", "Peter Saddow")
		};
		msg.AddTos(recipients);

		msg.SetSubject("Testing the SendGrid C# Library");

		msg.AddContent(MimeType.Text, "Hello World plain text!");
		msg.AddContent(MimeType.Html, "<p>Hello World!</p>");
		```
* Send an Email:
	* Send an email using SendGrid's API or .NET's build in library. 
	*  Send email from ASP .NET Core API using the `MailHelper` class

* Other options: 
	* Add an attachment
	* Enable footers, tracking and analytics
