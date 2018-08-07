---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a3d8a76905aa9abb0e5bf001688608e03446704a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812305"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**Относится к**: Outlook 
  
Создает именованный структуру, которая включает в себя структуру [DTBLGROUPBOX](dtblgroupbox.md) , содержащие элемент управления поля группы и метка заданной длины. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Длина подписи для поля группы. 
    
_u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Макрос **SizedDtblGroupBox** позволяет определить элемент управления поля группы при известные длина метки. Новая структура создается с следующие элементы: 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

Чтобы использовать указатель в итоговый структуру из макроса **SizedDtblGroupBox** как указатель на структуру **DTBLGROUPBOX** , выполните следующие приведения: 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>См. также

- [DTBLGROUPBOX](dtblgroupbox.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

