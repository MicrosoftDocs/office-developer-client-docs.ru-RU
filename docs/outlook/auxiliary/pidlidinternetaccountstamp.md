---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Возвращает штамп учетной записи учетной записи, доставить сообщение.
ms.openlocfilehash: c5da45268cefbe09588fdcfcda32e4e7a4be9d5f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390284"
---
# <a name="pidlidinternetaccountstamp"></a>PidLidInternetAccountStamp

Возвращает штамп учетной записи учетной записи, доставить сообщение.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidInetAcctStamp  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008581  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство должно содержать такое же значение, которое возвращается из API управления учетными данными свойство [PROP_ACCT_STAMP](prop_acct_stamp.md) для учетной записи, которые доставить сообщение. 
  
Поставщики хранилища сообщений предоставляют доступ к этой именованное свойство и [PidLidInternetAccountName](pidlidinternetaccountname.md) , чтобы выполняются перечисленные ниже действия: 
  
- Когда пользователь щелкает **Ответить всем** в сообщении электронной почты, Outlook удаляет адрес электронной почты, связанный с учетной записью и отметка на сообщение из списка получателей ответа. Эта проблема возникает, если этот адрес электронной почты отправителя сообщения. 
    
- По умолчанию Outlook отправляет ответов и пересылки сообщений через учетную запись, записывается исходного сообщения.
    
Как правило диспетчер протокола Outlook доставляет сообщения и Outlook задает свойств **PidLidInternetAccountName** и **PidLidInternetAccountStamp** , чтобы указать учетную запись, доставить сообщение. Тем не менее если хранилища сообщений тесно связан с транспорта, диспетчер протокола Outlook не доставлять сообщения и Outlook не удается задать эти свойства. В этом сценарии Outlook вызывает функцию [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) . Если поставщик хранения сообщений хочет эти именованные свойства, следует реализовать **IMAPIProp::GetIDsFromNames** и возврата теги свойства через параметр вывода *lppPropTags* . Outlook может затем вызвать метод [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) с помощью этих свойств теги и поставщика хранилища сообщений можно вернуть имя учетной записи и метка нужную учетную запись. 
  
Чтобы обеспечить поддержку этих именованных свойств, поставщиков хранилища следует ожидать Outlook использование **IMAPIProp::GetIDsFromNames** для получения тег свойства для этого свойства. Outlook задает следующие значения для структуры [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) , соответствующий этой именованного свойства, который передается как часть массива, на которую указывает входного параметра *lppPropNames* из **IMAPIProp::GetIDsFromNames**. 
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidInetAcctStamp  <br/> |
   
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)
- [Каноническое свойство PidLidInternetAccountStamp](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

