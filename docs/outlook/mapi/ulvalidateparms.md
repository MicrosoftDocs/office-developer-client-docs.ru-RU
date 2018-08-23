---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b71d1f477435b4a9327b4156560d1aa2e6079536
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578705"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Вызывает функцию внутреннего и проверять параметры клиентских приложений не имеет разрешений для поставщиков услуг и MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Параметры

 _eMethod_
  
> [in] Указывает перечисление, метод для проверки. 
    
 _Первый_
  
> [in] Указатель на первый аргумент в стеке.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_CALL_FAILED 
  
> Ошибка запрещено выполнение операции.
    
## <a name="remarks"></a>Замечания

Параметры, переданные между MAPI и службой поставщиков предполагается, что правильно и подвергаются только проверки отладка с помощью макроса [CheckParms](checkparms.md) . Поставщики должен проверить, все параметры, переданные в клиентских приложениях, но клиенты должны предполагается правильность параметров и MAPI. Использование макроса **HR_FAILED** для проверки возвращаемого значения. 
  
Макрос **UlValidateParms** называется по-разному в зависимости от того, является ли вызывающий кода C или C++. Этот макрос используется для проверки параметров несколько методы **IUnknown** и MAPI, которые возвращают ULONG вместо значения HRESULT; макрос [ValidateParms](validateparms.md) работает для всех других пользователей. 
  

