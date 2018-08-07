---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ae6f7d7066638ef1b149d3e411443384d531184d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808259"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Относится к**: Outlook 
  
Освобождает служебной программы функций, вызываемых явным образом с помощью функции [ScInitMapiUtil](scinitmapiutil.md) или неявно с помощью функции [MAPIInitialize](mapiinitialize.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a>Параметры

Нет 
  
## <a name="return-value"></a>������������ ��������

Нет 
  
## <a name="remarks"></a>Замечания

Функция **DeinitMapiUtil** release функции инициализации с [ScInitMapiUtil](scinitmapiutil.md) или [MAPIInitialize](mapiinitialize.md). 
  
По завершении работы функций, вызываемых **ScInitMapiUtil** **DeinitMapiUtil** необходимо явно вызывать для освобождения их. С другой стороны [MAPIUninitialize](mapiuninitialize.md) неявно вызывает **DeinitMapiUtil**. 
  

