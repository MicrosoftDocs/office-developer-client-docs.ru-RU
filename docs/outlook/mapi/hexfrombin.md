---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a1bf02de914865e27c8c018aba8695c858888ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412578"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Преобразует двоичное число в строку, представленную в hexadecimal number. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a>Параметры

 _pb_
  
> [in] Указатель на двоичные данные, которые необходимо преобразовать. 
    
 _cb_
  
> [in] Размер двоичных данных, на которые указывает параметр PB в _bytes._ 
    
 _sz_
  
> [out] Указатель на строку ASCII с нулью, представляющую двоичные данные в шесть цифр.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Функция **HexFromBin** принимает указатель на единицу двоичных данных, размер которых указывается параметром _cb._ Он возвращается в строке  _sz_ в пределах (2*  _cb_)+1 bytes памяти, представление этой двоичной информации в hexadecimal numbers. Если, например, значением в десятичной части является десятичная 10, то строка будет иметь значение 0A, поэтому один из них преобразуется в два в строке. 
  

