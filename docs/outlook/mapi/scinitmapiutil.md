---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351263"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Заменяет [мапиинитиализе](mapiinitialize.md) , когда используются только служебные функции SELECT. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Функции **сЦинитмапиутил** и [деинитмапиутил](deinitmapiutil.md) взаимодействуют для вызовов и выпуска выбранных служебных функций, в отличие от [мапиинитиализе](mapiinitialize.md), которые вызывают Core, а также служебные функции. Когда **сЦинитмапиутил** вызывает служебные функции, он также инициализирует требуемую память. 
  
При использовании функций, вызванных **сЦинитмапиутил** , метод **деинитмапиутил** необходимо вызывать явно, чтобы освободить их. В отличие от этого, **мапиинитиализе** неявно вызывает **деинитмапиутил**. 
  
## <a name="see-also"></a>См. также



[MAPIUninitialize](mapiuninitialize.md)

