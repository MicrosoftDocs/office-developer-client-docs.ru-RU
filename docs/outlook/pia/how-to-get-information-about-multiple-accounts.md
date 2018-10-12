---
title: Получение сведений о нескольких учетных записях
TOCTitle: Get information about multiple accounts
ms:assetid: 363f4058-3069-4ddc-b3ff-113a4dfd58c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184599(v=office.15)
ms:contentKeyID: 55119794
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 42d0d8439473e9404cb2e94ed9e7e83d59b4c95c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406689"
---
# <a name="get-information-about-multiple-accounts"></a><span data-ttu-id="09914-102">Получение сведений о нескольких учетных записях</span><span class="sxs-lookup"><span data-stu-id="09914-102">Get information about multiple accounts</span></span>

<span data-ttu-id="09914-103">Outlook поддерживает профиль, содержащий одну или несколько учетных записей, подключенных к серверу Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="09914-103">Microsoft Outlook supports a profile that contains one or more accounts that are connected to a Microsoft Exchange Server.</span></span> <span data-ttu-id="09914-104">В этом примере показано, как получать и отображать различные сведения о каждой учетной записи текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="09914-104">This example shows how to obtain and display miscellaneous information about each account in the current profile.</span></span>

## <a name="example"></a><span data-ttu-id="09914-105">Пример</span><span class="sxs-lookup"><span data-stu-id="09914-105">Example</span></span>

<span data-ttu-id="09914-p102">Следующий метод, EnumerateAccounts, отображает имя учетной записи, имя пользователя и SMTP-адрес для каждой учетной записи, определенной в текущем профиле. Если учетная запись подключена к серверу Exchange, EnumerateAccounts отображает имя и сведения о версии сервера Exchange. А если учетная запись находится в хранилище доставки, EnumerateAccounts отображает для учетной записи имя хранилища доставки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="09914-p102">The following method, EnumerateAccounts, displays the account name, user name, and Simple Mail Transfer Protocol (SMTP) address for each account that is defined in the current profile. If the account is connected to an Exchange server, EnumerateAccounts displays the Exchange server name and version information. And if the account resides on a delivery store, EnumerateAccounts displays the name of the default delivery store for the account.</span></span>

<span data-ttu-id="09914-109">EnumerateAccounts извлекает большую часть этих данных из объекта [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) кроме случая, когда объект **Account** не содержит сведений об имени пользователя и его SMTP-адресе.</span><span class="sxs-lookup"><span data-stu-id="09914-109"> accesses most of this information from the Account object, except when the Account object does not contain information about the user name and SMTP address.</span></span> <span data-ttu-id="09914-110">В этом случае EnumerateAccounts использует объекты [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) и [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="09914-110">In that case,   uses the AddressEntry and ExchangeUser objects.</span></span> 

<span data-ttu-id="09914-111">EnumerateAccounts получает объект **AddressEntry**, используя свойство [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)), получаемого из свойства [CurrentUser](https://msdn.microsoft.com/library/ff184864\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="09914-111"> obtains the AddressEntry object by using the AddressEntry property of the Recipient object obtained from the CurrentUser property.</span></span> <span data-ttu-id="09914-112">EnumerateAccounts получает объект **ExchangeUser**, используя метод [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) объекта **AddressEntry**.</span><span class="sxs-lookup"><span data-stu-id="09914-112"> obtains the ExchangeUser object by using the GetExchangeUser() method of the AddressEntry object.</span></span> 

<span data-ttu-id="09914-113">Алгоритм для получения различных сведений с помощью объектов Account, AddressEntry и ExchangeUser:</span><span class="sxs-lookup"><span data-stu-id="09914-113">The following is the algorithm to obtain various information by using the Account, AddressEntry, and ExchangeUser objects:</span></span>

- <span data-ttu-id="09914-114">Если объект **Account** содержит сведения об имени пользователя и его SMTP-адресе, используйте объект **Account** для отображения имени учетной записи, имени пользователя, SMTP-адреса, а также имени сервера Exchange и сведений о его версии, если учетная запись является учетной записью Exchange.</span><span class="sxs-lookup"><span data-stu-id="09914-114">If the **Account** object contains information about the user name and SMTP address, use the **Account** object to display the account name, user name, SMTP address, and Exchange server name and version information if the account is an Exchange account.</span></span>

- <span data-ttu-id="09914-115">Если объект **Account** не содержит сведений об имени пользователя и его SMTP-адресе, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="09914-115">If the **Account** object does not contain information about the user name and SMTP address, proceed as follows:</span></span>
    
  - <span data-ttu-id="09914-116">Если учетная запись не является учетной записью Exchange, используйте объект **AddressEntry** для отображения имени пользователя и SMTP-адреса.</span><span class="sxs-lookup"><span data-stu-id="09914-116">If the account is not an Exchange account, use the **AddressEntry** object to display the user name and SMTP address.</span></span>
    
  - <span data-ttu-id="09914-117">Если учетная запись является учетной записью Exchange, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="09914-117">If the account is an Exchange account, proceed as follows:</span></span>
        
    1.  <span data-ttu-id="09914-118">Используйте объект **Account** для отображения имени учетной записи, имени сервера Exchange и сведений о версии сервера Exchange.</span><span class="sxs-lookup"><span data-stu-id="09914-118">Use the **Account** object to display the account name, Exchange server name, and Exchange version information.</span></span>
        
    2.  <span data-ttu-id="09914-119">Используйте объект **ExchangeUser** для отображения имени пользователя и SMTP-адреса.</span><span class="sxs-lookup"><span data-stu-id="09914-119">Use the **ExchangeUser** object to display the user name and SMTP address.</span></span>

<span data-ttu-id="09914-120">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="09914-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="09914-121">Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="09914-121">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="09914-122">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="09914-122">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAccounts()
{
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    foreach (Outlook.Account account in accounts)
    {
        try
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Account: " + account.DisplayName);
            if (string.IsNullOrEmpty(account.SmtpAddress)
                || string.IsNullOrEmpty(account.UserName))
            {
                Outlook.AddressEntry oAE =
                    account.CurrentUser.AddressEntry
                    as Outlook.AddressEntry;
                if (oAE.Type == "EX")
                {
                    Outlook.ExchangeUser oEU =
                        oAE.GetExchangeUser()
                        as Outlook.ExchangeUser;
                    sb.AppendLine("UserName: " +
                        oEU.Name);
                    sb.AppendLine("SMTP: " +
                        oEU.PrimarySmtpAddress);
                    sb.AppendLine("Exchange Server: " +
                        account.ExchangeMailboxServerName);
                    sb.AppendLine("Exchange Server Version: " +
                        account.ExchangeMailboxServerVersion); 
                }
                else
                {
                    sb.AppendLine("UserName: " +
                        oAE.Name);
                    sb.AppendLine("SMTP: " +
                        oAE.Address);
                }
            }
            else
            {
                sb.AppendLine("UserName: " +
                    account.UserName);
                sb.AppendLine("SMTP: " +
                    account.SmtpAddress);
                if(account.AccountType == 
                    Outlook.OlAccountType.olExchange)
                {
                    sb.AppendLine("Exchange Server: " +
                        account.ExchangeMailboxServerName);
                    sb.AppendLine("Exchange Server Version: " +
                        account.ExchangeMailboxServerVersion); 
                }
            }
            if(account.DeliveryStore !=null)
            {
                sb.AppendLine("Delivery Store: " +
                    account.DeliveryStore.DisplayName);
            }
            sb.AppendLine("---------------------------------");
            Debug.Write(sb.ToString());
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="09914-123">См. также</span><span class="sxs-lookup"><span data-stu-id="09914-123">See also</span></span>

- [<span data-ttu-id="09914-124">Учетные записи</span><span class="sxs-lookup"><span data-stu-id="09914-124">Accounts</span></span>](accounts.md)

