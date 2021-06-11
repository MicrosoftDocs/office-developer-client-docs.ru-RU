---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ffa1b596b2f60bce35f24df8a20326502be8165a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422280"
---
# <a name="checkparms"></a>CheckParms

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вызывает внутреннюю функцию для проверки параметров отладки в методах поставщика услуг, называемых MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Параметры

 _eMethod_
  
> [in] Указывает путем переумерия метод проверки. 
    
 _First_
  
> [in] Указатель на первый аргумент в стеке.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> The call succeeded.
    
## <a name="remarks"></a>Примечания

В отличие от макрос [ValidateParms](validateparms.md) и [UlValidateParms](ulvalidateparms.md) макрос, макрос **CheckParms** не выполняет полную проверку параметров. Параметры, переданные между MAPI и поставщиками услуг, считаются правильными, поэтому **CheckParms** выполняет проверку только отладки. 
  

