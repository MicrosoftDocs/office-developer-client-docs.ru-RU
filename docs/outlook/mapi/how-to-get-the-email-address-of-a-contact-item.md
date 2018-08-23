---
title: Получение адреса электронной почты из элемента контакта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: f9c6766c934632a83fa0388ac2bc4c2c397eead6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575555"
---
# <a name="get-the-email-address-of-a-contact-item"></a><span data-ttu-id="04fd4-103">Получение адреса электронной почты из элемента контакта</span><span class="sxs-lookup"><span data-stu-id="04fd4-103">Get the email address of a Contact item</span></span>

<span data-ttu-id="04fd4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04fd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04fd4-105">В этом разделе показано, как получить значение именованного свойства, который представляет адрес электронной почты Microsoft Outlook 2010 или Microsoft Outlook 2013 контакт элемента.</span><span class="sxs-lookup"><span data-stu-id="04fd4-105">This topic shows how to obtain the value of a named property that represents the email address of an Microsoft Outlook 2010 or Microsoft Outlook 2013 Contact item.</span></span>
  
<span data-ttu-id="04fd4-106">До трех адресов электронной почты можно связать с элементом контактов в Outlook 2010 и Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="04fd4-106">You can associate up to three email addresses with a Contact item in Outlook 2010 and Outlook 2013.</span></span> <span data-ttu-id="04fd4-107">Свойство объекта Outlook 2010 или Outlook 2013 **ContactItem** в объектной модели Outlook 2010 и Outlook 2013 соответствует каждого адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="04fd4-107">Each email address corresponds to a property of the Outlook 2010 or Outlook 2013 **ContactItem** object in the Outlook 2010 and Outlook 2013 object models.</span></span> <span data-ttu-id="04fd4-108">Внутренний для Outlook 2010 и Outlook 2013, адрес электронной почты также соответствует MAPI, именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="04fd4-108">Internal to Outlook 2010 and Outlook 2013, the email address also corresponds to a MAPI named property.</span></span> <span data-ttu-id="04fd4-109">Например первый адрес электронной почты контакта, соответствует свойству **Email1Address** **ContactItem** в объектной модели Outlook 2010 и Outlook 2013 и внутреннего [именованные Outlook 2010 и Outlook 2013 Каноническое свойство PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="04fd4-109">For example, the first email address of a contact corresponds to the **Email1Address** property of the **ContactItem** in the Outlook 2010 and Outlook 2013 object models, and the Outlook 2010 and Outlook 2013 internal named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).</span></span>
  
<span data-ttu-id="04fd4-110">Для получения значения элемента контакта адрес электронной почты, можно использовать объект **PropertyAccessor** объектной модели Outlook 2010 или Outlook 2013 или сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства именованного свойства, а затем Укажите этот тег свойства в [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="04fd4-110">To obtain the value of an email address of a contact item, you can use the **PropertyAccessor** object of the Outlook 2010 or Outlook 2013 object model, or first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag of the named property, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="04fd4-111">При вызове **IMAPIProp::GetIDsFromNames**, укажите соответствующие значения для структуры [MAPINAMEID](mapinameid.md) , на которую указывает входного параметра _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="04fd4-111">When calling **IMAPIProp::GetIDsFromNames**, specify the appropriate values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_.</span></span> <span data-ttu-id="04fd4-112">В следующем примере кода показано, как получить первый адрес электронной почты указанного контакта `lpContact`, с помощью **GetIDsFromNames** и **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="04fd4-112">The following code sample shows how to obtain the first email address of a specified contact,  `lpContact`, using **GetIDsFromNames** and **GetProps**.</span></span> 
  
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


