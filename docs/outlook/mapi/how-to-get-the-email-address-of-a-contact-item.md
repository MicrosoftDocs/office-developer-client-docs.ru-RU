---
title: Получение электронного адреса элемента контакта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: 'Дата последнего изменения: 25 июня 2012 года'
ms.openlocfilehash: f9c6766c934632a83fa0388ac2bc4c2c397eead6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575555"
---
# <a name="get-the-email-address-of-a-contact-item"></a>Получение электронного адреса элемента контакта

**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе показано, как получить значение именованного свойства, который представляет адрес электронной почты Microsoft Outlook 2010 или Microsoft Outlook 2013 контакт элемента.
  
До трех адресов электронной почты можно связать с элементом контактов в Outlook 2010 и Outlook 2013. Свойство объекта Outlook 2010 или Outlook 2013 **ContactItem** в объектной модели Outlook 2010 и Outlook 2013 соответствует каждого адреса электронной почты. Внутренний для Outlook 2010 и Outlook 2013, адрес электронной почты также соответствует MAPI, именованное свойство. Например первый адрес электронной почты контакта, соответствует свойству **Email1Address** **ContactItem** в объектной модели Outlook 2010 и Outlook 2013 и внутреннего [именованные Outlook 2010 и Outlook 2013 Каноническое свойство PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md).
  
Для получения значения элемента контакта адрес электронной почты, можно использовать объект **PropertyAccessor** объектной модели Outlook 2010 или Outlook 2013 или сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства именованного свойства, а затем Укажите этот тег свойства в [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения. При вызове **IMAPIProp::GetIDsFromNames**, укажите соответствующие значения для структуры [MAPINAMEID](mapinameid.md) , на которую указывает входного параметра _lppPropNames_. В следующем примере кода показано, как получить первый адрес электронной почты указанного контакта `lpContact`, с помощью **GetIDsFromNames** и **GetProps**. 
  
```cpp
HRESULT HrGetEmail1(LPMESSAGE lpContact) 
{ 
    HRESULT hRes = S_OK; 
    LPSPropTagArray lpNamedPropTags = NULL; 
    MAPINAMEID NamedID = {0}; 
    LPMAPINAMEID lpNamedID = &NamedID; 
    NamedID.lpguid = (LPGUID)&PSETID_Address; 
    NamedID.ulKind = MNID_ID; 
    NamedID.Kind.lID = dispidEmailEmailAddress; 
 
    hRes = lpContact->GetIDsFromNames( 
           1,  
           &lpNamedID,  
           NULL,  
           &lpNamedPropTags); 
 
    if (SUCCEEDED(hRes) && lpNamedPropTags) 
    { 
        SPropTagArray sPropTagArray; 
 
        sPropTagArray.cValues = 1; 
        sPropTagArray.aulPropTag[0] = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[0],PT_STRING8); 
        LPSPropValue lpProps = NULL; 
        ULONG cProps = 0; 
 
        hRes = lpContact->GetProps( 
               &sPropTagArray, 
               NULL, 
               &cProps, 
               &lpProps); 
        if (SUCCEEDED(hRes) &&  
            1 == cProps &&  
            lpProps &&  
            PT_STRING8 == PROP_TYPE(lpProps[0].ulPropTag) && 
            lpProps[0].Value.lpszA) 
        { 
            printf("Email address 1 = \"%s\"\n",lpProps[0].Value.lpszA); 
        } 
        MAPIFreeBuffer(lpProps); 
        MAPIFreeBuffer(lpNamedPropTags); 
     } 
     return hRes; 
}
```


