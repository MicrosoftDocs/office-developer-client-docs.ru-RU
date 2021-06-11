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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420593"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Заменяет [MAPIInitialize при](mapiinitialize.md) только выборе полезных функций. 
  
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

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Функции **ScInitMapiUtil** и [DeinitMapiUtil](deinitmapiutil.md) взаимодействуют для вызова и выпуска функций выбора полезных функций, в отличие от [MAPIInitialize,](mapiinitialize.md)которая вызывает основные и полезные функции. Когда **ScInitMapiUtil** вызывает функции утилиты, он также инициализирует необходимую память. 
  
Когда использование функций, которые **вызвал ScInitMapiUtil,** завершено, для их освобождения необходимо явно присвоть **DeinitMapiUtil.** Напротив, **MAPIInitialize** неявно вызывает **DeinitMapiUtil**. 
  
## <a name="see-also"></a>См. также



[MAPIUninitialize](mapiuninitialize.md)

