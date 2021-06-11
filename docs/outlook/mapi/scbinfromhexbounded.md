---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439760"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Преобразует указанную часть строки представления гексадецимального номера в двоичный номер. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Parameters

 _sz_
  
> [in] Указатель на завершаемую строку null, которая должна быть преобразована. Допустимые символы включают гексадецимальные символы от 0 до 9, а также символы верхнего и нижнего регистра с помощью f.
    
 _pb_
  
> [вышел] Указатель на возвращенный двоичный номер.
    
 _cb_
  
> [in] Размер в bytes _параметра pb._ 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Преобразование было успешным.
    
MAPI_E_CALL_FAILED
  
> Были встречены недействительные символы.
    
## <a name="see-also"></a>См. также



[FBinFromHex](fbinfromhex.md)

