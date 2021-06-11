---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435224"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Находит первое возникновение подстройки null-terminated в строке null-terminated. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>Parameters

 _lpsz_
  
> [in] Указатель на строку null-terminated, которая будет искаться. Параметр  _lpsz_ не должен превышать 65536 символов. 
    
 _lpszKey_
  
> [in] Указатель на подстройку с недействимой, для поиска. Параметр  _lpszKey_ не должен превышать 65536 символов. 
    
## <a name="return-value"></a>Возвращаемое значение

 **SzFindSz** возвращает указатель на первый символ первого появления подстройки в строке. Если подстройка не возникает нигде в строке, если  _размер lpszKey_ превышает  _lpsz,_ или если любой параметр NULL, возвращается значение NULL. 
  
## <a name="remarks"></a>Примечания

Функция **SzFindSz** ищет только точный совпадение; он чувствителен к различиям в случае и диакритических различиях. Поддерживаются поиски в форматах Unicode и DBCS. Ограничение длины для обоих параметров имеется в символах, а не обязательно в bytes. 
  

