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
ms.openlocfilehash: b236b24c10a241dbdecc28bf2e04de5f69e989e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809867"
---
# <a name="mapigetdefaultmalloc"></a>MAPIGetDefaultMalloc

  
  
**Относится к**: Outlook 
  
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
  

