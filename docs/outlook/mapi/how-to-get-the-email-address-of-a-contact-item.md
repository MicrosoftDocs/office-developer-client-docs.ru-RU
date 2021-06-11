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

**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе показано, как получить значение имени свойства, которое представляет адрес электронной почты элемента Microsoft Outlook 2010, русская версия или Microsoft Outlook 2013 contact.
  
В 2010 и Outlook 2013 года можно связать до трех адресов электронной почты с элементом Outlook Contact. Каждый адрес электронной почты соответствует свойству объекта **contactItem** 2010 Outlook или Outlook 2013 г. в объектных моделях Outlook и Outlook 2013 г. Внутренний Outlook 2010 и Outlook 2013, адрес электронной почты также соответствует свойству MAPI с именем. Например, первый адрес электронной почты контакта соответствует свойству **Email1Address** **contactItem** в объектных моделях Outlook и Outlook 2013 г., а также внутренним свойствам Outlook и Outlook 2013 г. с именем [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).
  
Чтобы получить значение адреса электронной почты контактного элемента, можно использовать объект **PropertyAccessor** объект объектной модели Outlook 2010 или Outlook 2013 г., или сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства имени, а затем указать этот тег свойства в [IMAPIProp:GetProps](imapiprop-getprops.md) для получения значения. При вызове **IMAPIProp::GetIDsFromNames** укажите соответствующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает параметр _ввода lppPropNames._ В следующем примере кода показано, как получить первый адрес электронной почты указанного контакта с помощью `lpContact` **GetIDsFromNames** и **GetProps.** 
  
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


