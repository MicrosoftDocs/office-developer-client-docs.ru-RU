---
title: Получение электронного адреса элемента контакта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: fab09d0c594bac1374973f523abe6ff0b9c09dd0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429595"
---
# <a name="get-the-email-address-of-a-contact-item"></a>Получение электронного адреса элемента контакта

**Относится к**: Outlook 2013 | Outlook 2016 
  
В этом разделе показано, как получить значение именованного свойства, представляющего адрес электронной почты для элемента контакта Microsoft Outlook 2010 или Microsoft Outlook 2013.
  
Вы можете сопоставить до трех адресов электронной почты с элементом Contact в Outlook 2010 и Outlook 2013. Каждый адрес электронной почты соответствует свойству объекта **ContactItem** Outlook 2010 или Outlook 2013 в объектных моделях Outlook 2010 и Outlook 2013. Внутренний адрес Outlook 2010 и Outlook 2013 адрес электронной почты также соответствует именованному свойству MAPI. Например, первый адрес электронной почты контакта соответствует свойству **Email1Address** объекта **ContactItem** в объектной модели outlook 2010 и Outlook 2013, а также в outlook 2010 и Outlook 2013 Internal Name [ Каноническое свойство PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md).
  
Чтобы получить значение электронного адреса элемента Contact, можно использовать объект **PropertyAccessor** объектной модели Outlook 2010 или Outlook 2013 или сначала использовать [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , чтобы получить тег свойства именованного свойства, а затем Укажите этот тег свойства в [IMAPIProp::](imapiprop-getprops.md) /Props, чтобы получить значение. При вызове **IMAPIProp:: жетидсфромнамес**укажите соответствующие значения для структуры [мапинамеид](mapinameid.md) , на которую указывает входный параметр _лпппропнамес_. В приведенном ниже примере кода показано, как получить первый адрес электронной почты указанного контакта `lpContact`, используя **жетидсфромнамес** и **PROPS**. 
  
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


