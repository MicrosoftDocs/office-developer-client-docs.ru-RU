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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор записи глобальной адресной книги для Exchange службы _pEmsmdbUID._ Идентификатор возвращаемой записи должен быть освобожден с помощью [MAPIFreeBuffer.](mapifreebuffer.md)
  
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

## <a name="parameters"></a>Parameters

 _pSess_
  
> [in] Вход в систему IMAPISession. Это не может быть NULL.
    
 _pAddrBook_
  
> [in] Адресная книга, используемая для открытия идентификатора записи. Это не может быть NULL.
    
 _pEmsmdbUID_
  
> [in] Указатель на **emsmdbUID,** который определяет gal службы Exchange, которая должна быть извлечена. Если _pEmsmdbUID_ является NULL или нулевой UID, эта функция получает устаревшую ГАЛ службы Exchange. 
    
 _lpcbeid_
  
> [вышел] Указатель на количество byte идентификатора входа глобального списка адресов.
    
 _lppeid_
  
> [вышел] Указатель на идентификатор записи глобального списка адресов. Это должно быть освобождено с [помощью MAPIFreeBuffer](mapifreebuffer.md).
    

