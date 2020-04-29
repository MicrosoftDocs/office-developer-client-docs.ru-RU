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
  
Преобразует двоичное число в строковое представление шестнадцатеричного числа. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
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
  
> возврата Указатель на двоичные данные, которые необходимо преобразовать. 
    
 _cb_
  
> возврата Размер (в байтах) двоичных данных, на которые указывает параметр _Pb_ . 
    
 _сз_
  
> вышли Указатель на строку ASCII с завершающим нулем, представляющую двоичные данные в шестнадцатеричных цифрах.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Функция **хексфромбин** принимает указатель на единицу двоичных данных, размер которых указан параметром _CB_ . Он возвращается в строке _СЗ_ в пределах (2 * _CB_) + 1 байта памяти, представление двоичных данных в шестнадцатеричных числах. Если значение byte равно 10, например, шестнадцатеричная строка будет 0A, то один байт преобразуется в два байта в строке. 
  

