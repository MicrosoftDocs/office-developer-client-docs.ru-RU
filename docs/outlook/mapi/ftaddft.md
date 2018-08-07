---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e0e1535a770d4f1b437faf6a90c5f6415f6000ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808520"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**Относится к**: Outlook 
  
Добавление одного целых 64-разрядная версия на другой.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>Параметры

 _Addend1_
  
> [in] Структура [FILETIME](filetime.md) , содержащую первого целого числа без знака 64-разрядная версия будет добавлена. 
    
 _Addend2_
  
> [in] Структура **FILETIME** , содержащий второй целого числа без знака 64-разрядная версия будет добавлена. 
    
## <a name="return-value"></a>������������ ��������

Функция **FtAddFt** возвращает структуру **FILETIME** , содержащую сумма двух целых чисел. Два входных параметра не изменяются. 
  

