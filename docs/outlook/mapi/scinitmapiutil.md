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
ms.openlocfilehash: 771b466e58bf57a7eb4285c6f6ce94c815ec7288
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812201"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**Относится к**: Outlook 
  
Заменяет [MAPIInitialize](mapiinitialize.md) при использовании только функции select служебной программы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Функции **ScInitMapiUtil** и [DeinitMapiUtil](deinitmapiutil.md) сотрудничать для вызова и освобождать функции функции, в отличие от [MAPIInitialize](mapiinitialize.md), который вызывает основной, а также служебной программы выберите программы. Когда **ScInitMapiUtil** вызывает функции служебной программы, он также инициализирует необходимые памяти. 
  
По завершении использования функций, которые вызвали **ScInitMapiUtil** **DeinitMapiUtil** необходимо явно вызывать для освобождения их. С другой стороны **MAPIInitialize** неявно вызывает **DeinitMapiUtil**. 
  
## <a name="see-also"></a>См. также



[MAPIUninitialize](mapiuninitialize.md)

