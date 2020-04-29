---
title: имапиформконтаинержетластеррор
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetLastError
api_type:
- COM
ms.assetid: 04952b51-f005-4933-a1d1-695c6dc736cc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e020c66a46f1f195a5731ef1cb3f4b0488162a2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415672"
---
# <a name="imapiformcontainergetlasterror"></a>IMAPIFormContainer::GetLastError

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, созданной объектом контейнера формы. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _Состав_
  
> возврата Тип данных HRESULT, который содержит значение ошибки, возникшей при предыдущем вызове метода.
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющих тип возвращаемых строк. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре [мапиеррор](mapierror.md) , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI. 
    
 _лппмапиеррор_
  
> вышли Указатель на указатель на возвращаемую структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки. Параметр _лппмапиеррор_ может иметь значение null, если структура **мапиеррор** для возврата отсутствует. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Установлен флаг MAPI_UNICODE, а **GetLastError** не поддерживает Юникод, или MAPI_UNICODE не задано, а **GetLastError** поддерживает только Юникод. 
    
## <a name="remarks"></a>Примечания

Метод **имапиформконтаинер:: GetLastError** предоставляет сведения о предыдущем вызове метода, который завершился сбоем. Вызывающие абоненты могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **мапиеррор** в диалоговом окне. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать структуру **мапиеррор** , на которую указывает параметр _ЛППМАПИЕРРОР_ , если MAPI поддерживает один, только если **GetLastError** возвращает S_OK. Иногда MAPI не может определить, в чем последняя ошибка, или больше не сообщает об ошибке. В этом случае указатель на NULL возвращается в _лппмапиеррор_ . 
  
Более подробную информацию о методе **GetLastError** можно узнать [в статье Использование расширенных ошибок](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

