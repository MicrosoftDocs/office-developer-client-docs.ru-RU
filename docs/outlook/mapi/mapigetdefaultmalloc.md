---
title: MAPIGetDefaultMalloc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIGetDefaultMalloc
api_type:
- HeaderDef
ms.assetid: 148695dd-d886-4a06-9cfe-749059ae91ed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cb0630ba30f8d3d7ae38c165c5da60bbc12077c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592334"
---
# <a name="mapigetdefaultmalloc"></a>MAPIGetDefaultMalloc

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Получает адрес функции выделения памяти MAPI по умолчанию.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a>Параметры

Нет. 
  
## <a name="return-value"></a>Возвращаемое значение

Функция **MAPIGetDefaultMalloc** возвращает указатель на функцию выделения памяти MAPI по умолчанию. 
  

