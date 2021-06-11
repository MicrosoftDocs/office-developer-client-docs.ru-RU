---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f22d30c1bc7c797834f58bcd1306b14ac2542c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421258"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поиск последнего появления символа в строке с null-terminated. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Parameters

 _lpsz_
  
> [in] Указатель на строку null-terminated, которая будет искаться. 
    
 _ch_
  
> [in] Символ, который нужно искать.
    
## <a name="return-value"></a>Возвращаемое значение

 **SzFindLastCh** возвращает указатель к последнему появлению символа в строке. Если символ не встречается нигде в строке, или если параметр  _lpsz_ является NULL, возвращается значение NULL. 
  
## <a name="remarks"></a>Примечания

Функция **SzFindLastCh** ищет только точное совпадение; он чувствителен к различиям в случае и диакритических различиях. Поддерживаются поиски в форматах Unicode и DBCS. 
  

