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
ms.openlocfilehash: a00a9b2200f76dfd600f72bf387467b5792599c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812184"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**Относится к**: Outlook 
  
Преобразует указанную часть строковое представление шестнадцатеричное число в двоичное. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Параметры

 _sz_
  
> [in] Указатель на строку символом null, которую нужно преобразовать. Допустимые знаки включают шестнадцатеричных знаков 0 до 9 и прописные и строчные буквы по f.
    
 _pb_
  
> [out] Указатель на возвращаемый двоичное число.
    
 _cb_
  
> [in] Размер, в байтах, параметр _pb_ . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Преобразование прошло успешно.
    
MAPI_E_CALL_FAILED
  
> Обнаружены недопустимые символы.
    
## <a name="see-also"></a>См. также



[FBinFromHex](fbinfromhex.md)

