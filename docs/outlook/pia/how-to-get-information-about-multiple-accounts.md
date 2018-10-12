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
# <a name="get-information-about-multiple-accounts"></a>Получение сведений о нескольких учетных записях

Outlook поддерживает профиль, содержащий одну или несколько учетных записей, подключенных к серверу Exchange Server. В этом примере показано, как получать и отображать различные сведения о каждой учетной записи текущего профиля.

## <a name="example"></a>Пример

Следующий метод, EnumerateAccounts, отображает имя учетной записи, имя пользователя и SMTP-адрес для каждой учетной записи, определенной в текущем профиле. Если учетная запись подключена к серверу Exchange, EnumerateAccounts отображает имя и сведения о версии сервера Exchange. А если учетная запись находится в хранилище доставки, EnumerateAccounts отображает для учетной записи имя хранилища доставки по умолчанию.

EnumerateAccounts извлекает большую часть этих данных из объекта [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) кроме случая, когда объект **Account** не содержит сведений об имени пользователя и его SMTP-адресе. В этом случае EnumerateAccounts использует объекты [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) и [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)). 

EnumerateAccounts получает объект **AddressEntry**, используя свойство [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)), получаемого из свойства [CurrentUser](https://msdn.microsoft.com/library/ff184864\(v=office.15\)). EnumerateAccounts получает объект **ExchangeUser**, используя метод [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) объекта **AddressEntry**. 

Алгоритм для получения различных сведений с помощью объектов Account, AddressEntry и ExchangeUser:

- Если объект **Account** содержит сведения об имени пользователя и его SMTP-адресе, используйте объект **Account** для отображения имени учетной записи, имени пользователя, SMTP-адреса, а также имени сервера Exchange и сведений о его версии, если учетная запись является учетной записью Exchange.

- Если объект **Account** не содержит сведений об имени пользователя и его SMTP-адресе, выполните следующие действия:
    
  - Если учетная запись не является учетной записью Exchange, используйте объект **AddressEntry** для отображения имени пользователя и SMTP-адреса.
    
  - Если учетная запись является учетной записью Exchange, выполните следующие действия:
        
    1.  Используйте объект **Account** для отображения имени учетной записи, имени сервера Exchange и сведений о версии сервера Exchange.
        
    2.  Используйте объект **ExchangeUser** для отображения имени пользователя и SMTP-адреса.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Учетные записи](accounts.md)

