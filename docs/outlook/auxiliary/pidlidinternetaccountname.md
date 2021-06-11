---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Возвращает имя отображения учетной записи, которая передала сообщение.
ms.openlocfilehash: 2bd27cc7f868fb3f255a002ed70d0cb9b79516e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327687"
---
# <a name="pidlidinternetaccountname"></a>PidLidInternetAccountName

Возвращает имя отображения учетной записи, которая передала сообщение.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidInetAcctName  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008580  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно содержать то же значение, которое возвращается из свойства API управления учетной записью PROP_ACCT_NAME для учетной записи, которая доставляла сообщение. [](prop_acct_name.md) 
  
Поставщики магазинов сообщений раскрывают это свойство с именем [PidLidInternetAccountStamp,](pidlidinternetaccountstamp.md) чтобы были следующие действия: 
  
- Когда пользователь нажимает кнопку Ответ на все в сообщении электронной почты, Outlook удаляет адрес электронной почты, связанный с учетной записью и штампуется в сообщении из списка получателей ответа.  Такое поведение происходит, если этот адрес электронной почты не является отправивлю исходного сообщения. 
    
- По умолчанию Outlook отправляет ответы и отправляет сообщения через учетную запись, штампуемую в исходном сообщении.
    
Обычно диспетчер Outlook протоколов доставляет сообщения, а Outlook задает свойства **PidLidInternetAccountName** и **PidLidInternetAccountStamp,** чтобы указать учетную запись, которая передала сообщение. Однако если хранилище сообщений тесно совмещение с транспортом, диспетчер протокола Outlook не доставляет сообщения, и Outlook не может задать эти свойства. В этом сценарии Outlook [вызывает функцию IMAPIProp::GetIDsFromNames.](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) Если поставщик магазина сообщений хочет раскрыть эти свойства, он должен реализовать **IMAPIProp::GetIDsFromNames** и вернуть теги свойств через параметр  *вывода lppPropTags*  . Outlook затем можно вызвать метод [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) с помощью этих тегов свойств, а поставщик магазина сообщений может вернуть имя учетной записи и печать нужной учетной записи. 
  
Чтобы поддерживать указанные свойства, поставщики магазинов должны ожидать, что Outlook использовать **IMAPIProp::GetIDsFromNames** для получения тега свойства для этого свойства. Outlook указывает следующие значения для структуры [MAPINAMEID,](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) соответствующей этому имени свойства, которое передается как часть массива, указанного в параметре *ввода lppPropNames* **IMAPIProp::GetIDsFromNames**. 
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidInetAcctName  <br/> |
   
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md)
- [Constants (Account management API)](constants-account-management-api.md)
- [Каноническое свойство PidLidInternetAccountName](https://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

