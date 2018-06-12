---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Возвращает отображаемое имя учетной записи, доставить сообщение.
ms.openlocfilehash: 223bc5bbd485426676376d94875274613ff59685
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807939"
---
# <a name="pidlidinternetaccountname"></a>PidLidInternetAccountName

Возвращает отображаемое имя учетной записи, доставить сообщение.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidInetAcctName  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008580  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Области:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство должно содержать такое же значение, которое возвращается из API управления учетными данными свойство [PROP_ACCT_NAME](prop_acct_name.md) для учетной записи, которые доставить сообщение. 
  
Поставщики хранилища сообщений предоставляют доступ к этой именованное свойство и [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) , чтобы выполняются перечисленные ниже действия: 
  
- Когда пользователь щелкает **Ответить всем** в сообщении электронной почты, Outlook удаляет адрес электронной почты, связанный с учетной записью и отметка на сообщение из списка получателей ответа. Эта проблема возникает, если этот адрес электронной почты отправителя сообщения. 
    
- По умолчанию Outlook отправляет ответов и пересылки сообщений через учетную запись, записывается исходного сообщения.
    
Как правило диспетчер протокола Outlook доставляет сообщения и Outlook задает свойств **PidLidInternetAccountName** и **PidLidInternetAccountStamp** , чтобы указать учетную запись, доставить сообщение. Тем не менее если хранилища сообщений тесно связан с транспорта, диспетчер протокола Outlook не доставлять сообщения и Outlook не удается задать эти свойства. В этом сценарии Outlook вызывает функцию [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) . Если поставщик хранения сообщений хочет эти именованные свойства, следует реализовать **IMAPIProp::GetIDsFromNames** и возврата теги свойства через параметр вывода *lppPropTags* . Outlook может затем вызвать метод [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) с помощью этих свойств теги и поставщика хранилища сообщений можно вернуть имя учетной записи и метка нужную учетную запись. 
  
Чтобы обеспечить поддержку этих именованных свойств, поставщиков хранилища следует ожидать Outlook использование **IMAPIProp::GetIDsFromNames** для получения тег свойства для этого свойства. Outlook задает следующие значения для структуры [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) , соответствующий этой именованного свойства, который передается как часть массива, на которую указывает входного параметра *lppPropNames* из **IMAPIProp::GetIDsFromNames**. 
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidInetAcctName  <br/> |
   
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)
- [Constants (Account management API)](constants-account-management-api.md)
- [Каноническое свойство PidLidInternetAccountName](http://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

