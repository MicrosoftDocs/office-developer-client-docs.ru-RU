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
# <a name="get-the-email-address-of-a-contact-item"></a><span data-ttu-id="c2841-103">Получение электронного адреса элемента контакта</span><span class="sxs-lookup"><span data-stu-id="c2841-103">Get the email address of a Contact item</span></span>

<span data-ttu-id="c2841-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2841-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2841-105">В этом разделе показано, как получить значение именоваемого свойства, которое представляет адрес электронной почты элемента Microsoft Outlook 2010, русская версия контакта Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="c2841-105">This topic shows how to obtain the value of a named property that represents the email address of an Microsoft Outlook 2010 or Microsoft Outlook 2013 Contact item.</span></span>
  
<span data-ttu-id="c2841-106">Вы можете связать до трех адресов электронной почты с элементом контакта в Outlook 2010 и Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="c2841-106">You can associate up to three email addresses with a Contact item in Outlook 2010 and Outlook 2013.</span></span> <span data-ttu-id="c2841-107">Каждый адрес электронной почты соответствует свойству объекта Outlook 2010 или Outlook 2013 **ContactItem** в объектных моделях Outlook 2010 и Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="c2841-107">Each email address corresponds to a property of the Outlook 2010 or Outlook 2013 **ContactItem** object in the Outlook 2010 and Outlook 2013 object models.</span></span> <span data-ttu-id="c2841-108">Внутренний адрес электронной почты в Outlook 2010 и Outlook 2013 также соответствует именоваемой свойству MAPI.</span><span class="sxs-lookup"><span data-stu-id="c2841-108">Internal to Outlook 2010 and Outlook 2013, the email address also corresponds to a MAPI named property.</span></span> <span data-ttu-id="c2841-109">Например, первый адрес электронной почты контакта соответствует свойству **Email1Address** объекта **ContactItem** в объектных моделях Outlook 2010 и Outlook 2013, а также внутреннему свойству Outlook 2010 и Outlook 2013 [PidLidEmail1EmailAddress.](pidlidemail1emailaddress-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c2841-109">For example, the first email address of a contact corresponds to the **Email1Address** property of the **ContactItem** in the Outlook 2010 and Outlook 2013 object models, and the Outlook 2010 and Outlook 2013 internal named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).</span></span>
  
<span data-ttu-id="c2841-110">Чтобы получить значение адреса электронной почты элемента контакта, можно использовать объект **PropertyAccessor** объектной модели Outlook 2010 или Outlook 2013 или сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства именуемого свойства, а затем указать этот тег свойства в [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить значение.</span><span class="sxs-lookup"><span data-stu-id="c2841-110">To obtain the value of an email address of a contact item, you can use the **PropertyAccessor** object of the Outlook 2010 or Outlook 2013 object model, or first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag of the named property, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="c2841-111">При вызове **IMAPIProp::GetIDsFromNames** укажите соответствующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает входной параметр _lppPropNames._</span><span class="sxs-lookup"><span data-stu-id="c2841-111">When calling **IMAPIProp::GetIDsFromNames**, specify the appropriate values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_.</span></span> <span data-ttu-id="c2841-112">В следующем примере кода показано, как получить первый адрес электронной почты указанного контакта с помощью `lpContact` **GetIDsFromNames** и **GetProps.**</span><span class="sxs-lookup"><span data-stu-id="c2841-112">The following code sample shows how to obtain the first email address of a specified contact,  `lpContact`, using **GetIDsFromNames** and **GetProps**.</span></span> 
  
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


