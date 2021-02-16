---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Возвращает отметку учетной записи, которая доставляла сообщение.
ms.openlocfilehash: c5da45268cefbe09588fdcfcda32e4e7a4be9d5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327729"
---
# <a name="pidlidinternetaccountstamp"></a>PidLidInternetAccountStamp

Возвращает отметку учетной записи, которая доставляла сообщение.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidInetAcctStamp  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008581  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно содержать то же значение, которое возвращается из свойства API управления учетными PROP_ACCT_STAMP для учетной записи, которая доставляла сообщение. [](prop_acct_stamp.md) 
  
Поставщики store сообщений выдают это именоватое свойство [и pidLidInternetAccountName,](pidlidinternetaccountname.md) чтобы можно было сделать следующее: 
  
- Когда пользователь нажимает кнопку **"Ответить** всем" в сообщении электронной почты, Outlook удаляет адрес электронной почты, связанный с учетной записью, и пометит его в списке получателей ответа. Такое поведение происходит, если только этот адрес электронной почты не является отправивщиком исходного сообщения. 
    
- По умолчанию Outlook отправляет ответы и перенаправил сообщения через учетную запись, которая помеяна в исходном сообщении.
    
Обычно диспетчер протоколов Outlook доставляет сообщения, а Outlook задает свойства **PidLidInternetAccountName** и **PidLidInternetAccountStamp,** чтобы указать учетную запись, которая передала сообщение. Однако если хранилище сообщений тесно совмещение с транспортом, диспетчер протоколов Outlook не доставляет сообщения и Outlook не может установить эти свойства. В этом сценарии Outlook вызывает функцию [IMAPIProp::GetIDsFromNames.](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) Если поставщику параметров хранения сообщений требуется показать эти именуемые свойства, он должен реализовать **IMAPIProp::GetIDsFromNames** и возвратить теги свойств с помощью выходного параметра *lppPropTags.* Затем Outlook может вызвать метод [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) с помощью этих тегов свойств, а поставщик store сообщений может вернуть имя учетной записи и метку нужной учетной записи. 
  
Чтобы поддерживать эти именуемые свойства, поставщики магазина должны ожидать, что Outlook будет использовать **IMAPIProp::GetIDsFromNames** для получения тега свойства для этого свойства. Outlook указывает следующие значения для структуры [MAPINAMEID,](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) соответствующей этому именоватому свойству, которое передается как часть массива, на который указывает входной параметр *lppPropNames* **IMAPIProp::GetIDsFromNames.** 
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidInetAcctStamp  <br/> |
   
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)
- [Каноническое свойство PidLidInternetAccountStamp](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

