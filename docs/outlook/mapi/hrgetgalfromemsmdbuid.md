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
  
Возвращает идентификатор глобальной адресной книги для службы Exchange, идентифицируемой _пемсмдбуид_. Возвращенный идентификатор элемента должен быть освобожден с помощью [мапифрибуффер](mapifreebuffer.md).
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |абхелп. h  <br/> |
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

 _Псесс_
  
> возврата Вошедший в систему IMAPISession. Он не может иметь значение NULL.
    
 _Паддрбук_
  
> возврата Адресная книга, используемая для открытия идентификатора записи. Он не может иметь значение NULL.
    
 _Пемсмдбуид_
  
> возврата Указатель на **емсмдбуид** , ОПРЕДЕЛЯЮЩий глобальную коллекцию адресов, которую необходимо получить. Если _пемсмдбуид_ имеет значение null или нулевой UID, эта функция получает глобальный список адресов (GAL) устаревшей службы Exchange. 
    
 _лпкбеид_
  
> вышли Указатель на число байтов идентификатора записи глобального списка адресов.
    
 _лппеид_
  
> вышли Указатель на идентификатор элемента глобального списка адресов. Его следует освободить с помощью [мапифрибуффер](mapifreebuffer.md).
    

