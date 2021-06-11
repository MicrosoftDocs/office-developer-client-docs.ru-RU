---
title: Отправка электронного сообщения по SMTP-адресу учетной записи
TOCTitle: Send an email given the SMTP address of an account
ms:assetid: 4ff4aaac-54ba-45c7-8b2e-aeba35af1e56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462095(v=office.15)
ms:contentKeyID: 55119865
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0771941581d0edaab1660790582cfb22bef48dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332097"
---
# <a name="send-an-email-given-the-smtp-address-of-an-account"></a><span data-ttu-id="7eeee-102">Отправка электронного сообщения по SMTP-адресу учетной записи</span><span class="sxs-lookup"><span data-stu-id="7eeee-102">Send an email given the SMTP address of an account</span></span>

<span data-ttu-id="7eeee-103">В этом разделе показывается создание сообщения электронной почты и его отправка из учетной записи Microsoft Outlook с использованием SMTP-адреса этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7eeee-103">This topic shows how to create an email and send it from a Microsoft Outlook account, given the Simple Mail Transfer Protocol (SMTP) address of that account.</span></span>

## <a name="example"></a><span data-ttu-id="7eeee-104">Пример</span><span class="sxs-lookup"><span data-stu-id="7eeee-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="7eeee-105">Приведенные ниже примеры кода создал Хельмут Обертаннер (Helmut Obertanner).</span><span class="sxs-lookup"><span data-stu-id="7eeee-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="7eeee-106">Хельмут специализируется на Outlook и инструментах разработчика Office для Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7eeee-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 


<span data-ttu-id="7eeee-107">В следующем примере кода используются методы SendEmailFromAccount и GetAccountForEmailAddress класса Sample, которые реализованы в рамках проекта надстройки Outlook.</span><span class="sxs-lookup"><span data-stu-id="7eeee-107">The following code examples contain the SendEmailFromAccount and GetAccountForEmailAddress methods of the Sample class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="7eeee-108">Каждый проект добавляет ссылку на основную сборку взаимодействия Outlook на основе пространства имен [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="7eeee-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span> <span data-ttu-id="7eeee-109">Метод SendEmailFromAccount принимает в качестве входных аргументов надежный объект [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) и строки, которые представляют тему, основной текст, разделенный точками с запятыми список получателей и SMTP-адрес учетной записи электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7eeee-109">The SendEmailFromAccount method accepts as input arguments a trusted [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object, and strings that represent the subject, body, a semicolon-delimited list of recipients, and the SMTP address of an email account.</span></span> <span data-ttu-id="7eeee-110">Метод SendEmailFromAccount создает объект [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) и инициализирует свойства [To](https://msdn.microsoft.com/library/bb624372\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) и [Body](https://msdn.microsoft.com/library/bb646600\(v=office.15\)) заданными аргументами.</span><span class="sxs-lookup"><span data-stu-id="7eeee-110">SendEmailFromAccount creates a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object and initializes the [To](https://msdn.microsoft.com/library/bb624372\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)), and [Body](https://msdn.microsoft.com/library/bb646600\(v=office.15\)) properties with the given arguments.</span></span> <span data-ttu-id="7eeee-111">Чтобы найти объект [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)), из которого нужно отправлять электронную почту, метод SendEmailFromAccount вызывает метод GetAccountForEmailAddress, сопоставляющий заданный SMTP-адрес со свойством [SmtpAddress](https://msdn.microsoft.com/library/bb623516\(v=office.15\)) каждой учетной записи текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="7eeee-111">To find the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object from which to send the email, SendEmailFromAccount calls the GetAccountForEmailAddress method, which matches the given SMTP address with the [SmtpAddress](https://msdn.microsoft.com/library/bb623516\(v=office.15\)) property of each account for the current profile.</span></span> <span data-ttu-id="7eeee-112">Соответствующий объект **Account** возвращается методу SendEmailFromAccount, который затем инициализирует свойство [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) объекта **MailItem** с этим объектом **Account** и отправляет объект **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="7eeee-112">The matching **Account** object is returned to SendEmailFromAccount, which then initializes the [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) property of the **MailItem** with this **Account** object, and sends the **MailItem**.</span></span>

<span data-ttu-id="7eeee-113">Ниже приведен пример кода на языке Visual Basic, за которым следует пример на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="7eeee-113">The following is the Visual Basic code example, followed by the C\# code example.</span></span>

<span data-ttu-id="7eeee-114">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="7eeee-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7eeee-115">Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="7eeee-115">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7eeee-116">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="7eeee-116">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        
        Shared Sub SendEmailFromAccount(ByVal application As Outlook.Application, _
            ByVal subject As String, ByVal body As String, ByVal recipients As String, ByVal smtpAddress As String)

            ' Create a new MailItem and set the To, Subject, and Body properties.
            Dim newMail As Outlook.MailItem = DirectCast(application.CreateItem(Outlook.OlItemType.olMailItem), Outlook.MailItem)
            newMail.To = recipients
            newMail.Subject = subject
            newMail.Body = body

            ' Retrieve the account that has the specific SMTP address.
            Dim account As Outlook.Account = GetAccountForEmailAddress(application, smtpAddress)
            ' Use this account to send the email.
            newMail.SendUsingAccount = account
            newMail.Send()
        End Sub

        Shared Function GetAccountForEmailAddress(ByVal application As Outlook.Application, ByVal smtpAddress As String) As Outlook.Account

            ' Loop over the Accounts collection of the current Outlook session.
            Dim accounts As Outlook.Accounts = application.Session.Accounts
            Dim account As Outlook.Account
            For Each account In accounts
                ' When the email address matches, return the account.
                If account.SmtpAddress = smtpAddress Then
                    Return account
                End If
            Next
            Throw New System.Exception(String.Format("No Account with SmtpAddress: {0} exists!", smtpAddress))
        End Function

    End Class
End Namespace
```


```csharp
using System;
using System.Text;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        public static void SendEmailFromAccount(Outlook.Application application, string subject, string body, string to, string smtpAddress)
        {

            // Create a new MailItem and set the To, Subject, and Body properties.
            Outlook.MailItem newMail = (Outlook.MailItem)application.CreateItem(Outlook.OlItemType.olMailItem);
            newMail.To = to;
            newMail.Subject = subject;
            newMail.Body = body;

            // Retrieve the account that has the specific SMTP address.
            Outlook.Account account = GetAccountForEmailAddress(application, smtpAddress);
            // Use this account to send the email.
            newMail.SendUsingAccount = account;
            newMail.Send();
        }


        public static Outlook.Account GetAccountForEmailAddress(Outlook.Application application, string smtpAddress)
        {

            // Loop over the Accounts collection of the current Outlook session.
            Outlook.Accounts accounts = application.Session.Accounts;
            foreach (Outlook.Account account in accounts)
            {
                // When the email address matches, return the account.
                if (account.SmtpAddress == smtpAddress)
                {
                    return account;
                }
            }
            throw new System.Exception(string.Format("No Account with SmtpAddress: {0} exists!", smtpAddress));
        }

    }
}
```

## <a name="see-also"></a><span data-ttu-id="7eeee-117">См. также</span><span class="sxs-lookup"><span data-stu-id="7eeee-117">See also</span></span>

- [<span data-ttu-id="7eeee-118">Почта</span><span class="sxs-lookup"><span data-stu-id="7eeee-118">Mail</span></span>](mail.md)

