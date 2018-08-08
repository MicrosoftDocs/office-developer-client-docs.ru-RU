---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0d8d1b8509f699b20f6e436d8af2c1d0d97cf4ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808425"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**Относится к**: Outlook 
  
Определяет, одинаковы ли два MAPI с именем свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>Параметры

 _lpName1_
  
> [in] Указатель на структуру [MAPINAMEID](mapinameid.md) , описывающий первый именованное свойство. 
    
 _lpName2_
  
> [in] Указатель на структуру **MAPINAMEID** , описывающее второй именованное свойство. 
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Имена двух свойство равны. 
    
FALSE 
  
> Имена двух свойств не совпадают.
    
## <a name="remarks"></a>Замечания

Функция **FEqualNames** полезен, так как структура **MAPINAMEID** содержит [идентификатор GUID](guid.md) и может представлять имя свойства в несколько способов. Это означает, что две структуры нельзя сравнивать простой двоичные методами. 
  
Процесс тестирования задается с учетом регистра для строк имя свойства. 
  

