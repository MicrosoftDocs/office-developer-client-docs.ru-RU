---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 64d205ee7f51c0ce6a6eb1e982659c6cda675f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808434"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**Относится к**: Outlook 
  
Преобразует строковое представление шестнадцатеричного числа в двоичных данных. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Параметры

 _sz_
  
> [in] Указатель на строку ASCII символом null, которую нужно преобразовать. Не является строка Юникода. Допустимые знаки включают шестнадцатеричных знаков нулевой до девяти как, так и прописные и строчные буквы A до F.
    
 _pb_
  
> [out] Указатель на возвращаемый двоичное число.
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Строка была успешно преобразуется в двоичное. 
    
FALSE 
  
> Входная строка содержит недопустимый шестнадцатеричных знаков ASCII.
    
## <a name="see-also"></a>См. также



[ScBinFromHexBounded](scbinfromhexbounded.md)

