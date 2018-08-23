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
ms.openlocfilehash: 8f68de5e18d84c728241c188b932f99456f5be8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584837"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Преобразует двоичное число в строковое представление шестнадцатеричного числа. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a>Параметры

 _pb_
  
> [in] Указатель на преобразование двоичных данных. 
    
 _cb_
  
> [in] Размер, в байтах, двоичных данных, на который указывает параметр _pb_ . 
    
 _sz_
  
> [out] Указатель на строку ASCII символом null, представляющее двоичные данные в шестнадцатеричных цифр.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Функция **HexFromBin** принимает указатель на единицу двоичные данные, размер которых указывается с помощью параметра _Сертификация_ . Возвращает в строке _sz_ внутри (2 * _Сертификация_) + 1 байт памяти, представление двоичных данных в шестнадцатеричными числами. Если значение типа byte десятичное число 10, например, шестнадцатеричную строку будет 0A, преобразуется в таком один байт два байта в строке. 
  

