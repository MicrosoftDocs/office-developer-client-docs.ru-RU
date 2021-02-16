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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выполняет поиск последнего вхождения символа в строке с нулью. 
  
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

## <a name="parameters"></a>Параметры

 _lpsz_
  
> [in] Указатель на строку, о конце null для поиска. 
    
 _ch_
  
> [in] Ищите символ.
    
## <a name="return-value"></a>Возвращаемое значение

 **SzFindLastCh** возвращает указатель на последний вхождение символа в строке. Если символ не встречается ни в одной строке или если параметр  _lpsz_ имеет значение NULL, возвращается значение NULL. 
  
## <a name="remarks"></a>Примечания

Функция **SzFindLastCh** ищет только точное совпадение; он чувствителен к различиям в диакритических и диакритических диакритах. Поиск в форматах Юникод и DBCS поддерживается. 
  

