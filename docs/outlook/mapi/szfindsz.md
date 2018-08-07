---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0cc8f25271d1494ebdaca82caa2e77839f299276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812455"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**Относится к**: Outlook 
  
Поиск первого вхождения подстроки символом null в строку символом null. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>Параметры

 _lpsz_
  
> [in] Указатель на строку символом null для поиска. Параметр _lpsz_ не должен превышать 65536 символов. 
    
 _lpszKey_
  
> [in] Указатель на подстроки символом null для поиска. Параметр _lpszKey_ не должен превышать 65536 символов. 
    
## <a name="return-value"></a>������������ ��������

 **SzFindSz** возвращает указатель на первый символ первого вхождения подстроки в строке. Если подстрока не происходит в строке, в любом месте, если _lpszKey_ больше, чем _lpsz_или один из параметров имеет значение NULL, возвращается значение NULL. 
  
## <a name="remarks"></a>Замечания

Функция **SzFindSz** выполняется поиск точного совпадения. Это зависит от регистра и диакритических различия. Поиск в форматах Юникод и DBCS поддерживаются. Ограничение длины на оба параметра — в символы, не обязательно в байтах. 
  

