---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406019"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Дублирует массив значений свойства в отдельном блоке памяти MAPI, сочетая операции функций [сккопипропс](sccopyprops.md) и [сккаунтпропс](sccountprops.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a>Параметры

 _кпроп_
  
> возврата Количество значений свойств в массиве, указанном с помощью параметра _ргпроп_ . 
    
 _ргпроп_
  
> возврата Указатель на массив структур [спропвалуе](spropvalue.md) , определяющий значения свойств, которые должны дублироваться. 
    
 _Лпаллокатебуффер_
  
> возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться для выделения памяти для дублированного массива. 
    
 _пргпроп_
  
> вышли Указатель на начальную позицию в памяти, в которой хранится возвращенный повторяющийся массив структур **спропвалуе** . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    

