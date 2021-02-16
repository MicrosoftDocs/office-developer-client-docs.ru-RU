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
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439109"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор записи глобальной адресной книги для службы Exchange, определяемой _pEmsmdbUID._ Возвращаемого идентификатора записи следует освободить с помощью [MAPIFreeBuffer](mapifreebuffer.md).
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
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
  
> [in] Во время входа в систему IMAPISession. Это не может быть NULL.
    
 _pAddrBook_
  
> [in] Адресная книга, используемая для открытия идентификатора записи. Это не может быть NULL.
    
 _pEmsmdbUID_
  
> [in] Указатель на **emsmdbUID,** который определяет gal извлекаемой службы Exchange. Если  _pEmsmdbUID_ имеет значение NULL или нулевое значение UID, эта функция получает устаревший gal службы Exchange. 
    
 _lpcbeid_
  
> [out] Указатель на количество byte идентификатора записи глобального списка адресов.
    
 _lppeid_
  
> [out] Указатель на идентификатор записи глобального списка адресов. Его следует освободить с помощью [MAPIFreeBuffer.](mapifreebuffer.md)
    

