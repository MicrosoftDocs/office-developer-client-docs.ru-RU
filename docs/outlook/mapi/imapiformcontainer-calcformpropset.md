---
title: имапиформконтаинеркалкформпропсет
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ec1933f80f211c7c381f9de6b15d414932b9a78e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414916"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает массив свойств, используемых всеми формами, установленными в контейнере форм.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, определяющих, как возвращается массив свойств в параметре _ппресултс_ . Можно задать следующие флаги: 
    
FORMPROPSET_INTERSECTION 
  
> Возвращаемый массив содержит пересечение свойств формы.
    
FORMPROPSET_UNION 
  
> Возвращаемый массив содержит объединение свойств Forms.
    
MAPI_UNICODE 
  
> Возвращаемые в массиве строки представлены в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.
    
 _ппресултс_
  
> вышли Указатель на указатель на возвращаемую структуру [смапиформпропаррай](smapiformproparray.md) . Эта структура содержит все свойства, используемые установленными формами. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Установлен флаг MAPI_UNICODE, а реализация не поддерживает Юникод, или MAPI_UNICODE не задано, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Клиентские приложения вызывают метод **имапиформконтаинер:: калкформпропсет** для получения массива свойств, используемых всеми формами, установленными в контейнере форм. **Имапиформконтаинер:: калкформпропсет** работает аналогично методу [Имапиформмгр:: калкформпропсет](imapiformmgr-calcformpropset.md) , за исключением того, что он работает с каждой формой, зарегистрированной в определенном контейнере. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщики библиотеки форм, не поддерживающие строки Юникода, должны возвращать MAPI_E_BAD_CHARWIDTH, если MAPI_UNICODE передается.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **Имапиформконтаинер:: калкформпропсет** принимает либо пересечение, либо объединение наборов свойств формы, в зависимости от флага, установленного в параметре _ulFlags_ , и возвращает структуру **смапиформпропаррай** , содержащую результирующую группу свойств. 
  
Если клиент передает MAPI_UNICODEный флаг в _ulFlags_, все возвращенные строки имеют кодировку Юникод.
  
## <a name="see-also"></a>См. также



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

