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
ms.openlocfilehash: 6e616a76d9665b602184e88566384506fcce5697
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416078"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает объект фабрики классов для формы.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Параметры

 _clsidForm_
  
> [in] Идентификатор класса для формы, создаемой фабрикой классов.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lppClassFactory_
  
> [out] Указатель на объект фабрики классов.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Возвращен объект фабрики классов.
    
## <a name="remarks"></a>Примечания

Посетители форм звонят **методу IMAPIFormFactory::CreateClassFactory,** чтобы получить фабрику классов для определенной формы. Фабрика классов используется для создания экземпляров формы, которая обрабатывает сообщения определенного класса, и для управления доступом к этим экземплярам. 
  
Метод **CreateClassFactory** вызван с помощью программы просмотра форм, чтобы получить объект фабрики классов для серверов форм, которые реализуют несколько классов сообщений. Этот метод получает идентификатор класса (CLSID) в качестве параметра. На основе этого параметра этот метод может определить конкретный тип возвращаемого объекта фабрики классов. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вы можете вернуть из реализации **CreateClassFactory** один и тот же объект фабрики класса при нескольких вызовах для одного и того же идентификатора класса. Создание экземпляра фабрики классов не требуется. 
  
Можно использовать реализацию фабрики с одним классом, которая создает соответствующие экземпляры фабрики классов по требованию, или несколько реализации фабрики классов по одному для каждого класса сообщения.
  
## <a name="see-also"></a>См. также



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

