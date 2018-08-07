---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c221f98d6551ea63971dd378d522c1f2bebb312b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812453"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**Относится к**: Outlook 
  
Выполняет поиск последнего вхождения знака в string символом null. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Параметры

 _lpsz_
  
> [in] Указатель на строку символом null для поиска. 
    
 _Кан_
  
> [in] Знак для поиска.
    
## <a name="return-value"></a>������������ ��������

 **SzFindLastCh** возвращает указатель на последнего вхождения знаков в строке. Если кодировка не происходит в любом месте в строке или параметр _lpsz_ имеет значение NULL, возвращается значение NULL. 
  
## <a name="remarks"></a>Замечания

Функция **SzFindLastCh** выполняется поиск точного совпадения. Это зависит от регистра и диакритических различия. Поиск в формате Юникод и DBCS поддерживаются. 
  

