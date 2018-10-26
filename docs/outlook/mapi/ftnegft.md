---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 37dc92a40043657cb791359d543ef52c77dbd8ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589240"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вычисляет два элемента дополнения из 64-разрядное целое число без знака. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>Параметры

 _FT_
  
> [in] Структура [FILETIME](filetime.md) , содержащую целых 64-разрядная версия, для которого нужно вычислить два элемента дополнения. 
    
## <a name="return-value"></a>Возвращаемое значение

Функция **FtNegFt** возвращает структуру **FILETIME** , содержащую два элемента дополнения целого числа. Входной параметр остается неизменным. 
  

