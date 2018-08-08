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
ms.openlocfilehash: e26acb8415df007a7f3fb5901521da7222ae40ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808528"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**Относится к**: Outlook 
  
Вычисляет два элемента дополнения из 64-разрядное целое число без знака. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>Параметры

 _FT_
  
> [in] Структура [FILETIME](filetime.md) , содержащую целых 64-разрядная версия, для которого нужно вычислить два элемента дополнения. 
    
## <a name="return-value"></a>������������ ��������

Функция **FtNegFt** возвращает структуру **FILETIME** , содержащую два элемента дополнения целого числа. Входной параметр остается неизменным. 
  

