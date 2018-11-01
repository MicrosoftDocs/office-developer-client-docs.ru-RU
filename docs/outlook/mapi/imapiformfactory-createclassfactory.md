---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cb5cb5a0169e716f7fcc7f596660bc0222c51c84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572160"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает объект фабрики класса для формы.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Параметры

 _clsidForm_
  
> [in] Идентификатор класса для формы будет создан с помощью класса.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lppClassFactory_
  
> [out] Указатель на объект фабрики класса.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Возвращает объект фабрики класса.
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IMAPIFormFactory::CreateClassFactory** для получения фабрики классов для определенной формы. Фабрика классов используется для создания экземпляров формы, которая обрабатывает сообщения определенного класса и для управления доступом к эти экземпляры. 
  
Метод **CreateClassFactory** вызывается средства просмотра формы для получения объекта фабрики класса для серверов форм, которые реализуют несколько классов сообщений. Этот метод получает идентификатор класса (CLSID) как параметр. На основе этого параметра, этот метод можно определить определенного вида объекта фабрики класса для возврата. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Можно вернуть от внедрения **CreateClassFactory** один и тот же объект фабрики класса на несколько вызовов для один и тот же идентификатор класса. Создание нового экземпляра класса фабрики не требуется. 
  
Может иметь реализацию фабрики одного класса, который создает экземпляры фабрики соответствующий класс по запросу или нескольких реализации фабрики классов, другая — для каждого класса сообщений.
  
## <a name="see-also"></a>См. также



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

