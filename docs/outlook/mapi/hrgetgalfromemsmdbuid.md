---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4b05baf1f819a821da3496cc63c2b2980894efd7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575716"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор записи из глобальной адресной книги для службы Exchange, определяемую средством _pEmsmdbUID_. Идентификатор записи возвращенные нужно освободить с помощью [MAPIFreeBuffer](mapifreebuffer.md).
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a>Параметры

 _pSess_
  
> [in] Система на IMAPISession. Он не может быть NULL.
    
 _pAddrBook_
  
> [in] В адресной книге используется для открытия идентификатор записи. Он не может быть NULL.
    
 _pEmsmdbUID_
  
> [in] Указатель на **emsmdbUID** , идентифицирующий глобального списка адресов Exchange службы нужно вернуть. Если _pEmsmdbUID_ имеет значение NULL или ноль UID, эта функция возвращает прежних версий из глобального списка адресов службы Exchange. 
    
 _lpcbeid_
  
> [out] Указатель на количество байтов идентификатор записи из глобального списка адресов.
    
 _lppeid_
  
> [out] Указатель на идентификатор записи из глобального списка адресов. Это нужно освободить с помощью [MAPIFreeBuffer](mapifreebuffer.md).
    

