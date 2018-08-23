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
ms.openlocfilehash: e84dbc0976f5c438a7e0b5fd7cddcbf1c0659f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574799"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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

None 
  
## <a name="return-value"></a>������������ ��������

Отсутствует 
  
## <a name="remarks"></a>Замечания

Функция **DeinitMapiUtil** release функции инициализации с [ScInitMapiUtil](scinitmapiutil.md) или [MAPIInitialize](mapiinitialize.md). 
  
По завершении работы функций, вызываемых **ScInitMapiUtil** **DeinitMapiUtil** необходимо явно вызывать для освобождения их. С другой стороны [MAPIUninitialize](mapiuninitialize.md) неявно вызывает **DeinitMapiUtil**. 
  

