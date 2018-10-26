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
ms.openlocfilehash: 3176280de33bda01bfd09ebaafc31d326d455a3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575037"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Заменяет [MAPIInitialize](mapiinitialize.md) при использовании только функции select служебной программы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Функции **ScInitMapiUtil** и [DeinitMapiUtil](deinitmapiutil.md) сотрудничать для вызова и освобождать функции функции, в отличие от [MAPIInitialize](mapiinitialize.md), который вызывает основной, а также служебной программы выберите программы. Когда **ScInitMapiUtil** вызывает функции служебной программы, он также инициализирует необходимые памяти. 
  
По завершении использования функций, которые вызвали **ScInitMapiUtil** **DeinitMapiUtil** необходимо явно вызывать для освобождения их. С другой стороны **MAPIInitialize** неявно вызывает **DeinitMapiUtil**. 
  
## <a name="see-also"></a>См. также



[MAPIUninitialize](mapiuninitialize.md)

