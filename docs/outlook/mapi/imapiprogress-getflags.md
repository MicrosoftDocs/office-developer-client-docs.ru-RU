---
title: имапипрогрессжетфлагс
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423645"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает параметры флага из объекта Progress для уровня операции, на котором рассчитываются сведения о ходе выполнения.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _лпулфлагс_
  
> вышли Битовая маска флагов, которые управляют уровнем работы, на котором рассчитываются сведения о ходе выполнения. Можно вернуть следующий флаг:
    
MAPI_TOP_LEVEL 
  
> Выполняется вычисление хода выполнения для объекта верхнего уровня, объекта, вызываемого клиентом для начала операции. Например, объект верхнего уровня в операции копирования папки — это копируемая папка. Если MAPI_TOP_LEVEL не задано, выполняется вычисление хода выполнения для объекта нижнего уровня или подобъекта. В операции копирования папки объект нижнего уровня является одной из вложенных папок в копируемой папке.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Значение флагов успешно возвращено.
    
## <a name="remarks"></a>Примечания

MAPI позволяет поставщикам услуг различать объекты верхнего уровня и подобъекты с помощью флага MAPI_TOP_LEVEL, чтобы все объекты, участвующие в операции, могли использовать одну и ту же реализацию [IMAPIProgress](imapiprogressiunknown.md) для отображения хода выполнения. Это приводит к плавному отображению индикатора в отдельном положительном направлении. Установлен ли флаг MAPI_TOP_LEVEL определяет, как поставщики услуг устанавливают другие параметры при последующих вызовах объекта Progress. 
  
Значение, возвращаемое методом "- **flags** ", изначально задается средством реализации, а затем поставщиком услуг при вызове метода [IMAPIProgress:: SetLimits](imapiprogress-setlimits.md) . 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Всегда инициализируйте флаг, чтобы он MAPI_TOP_LEVEL, а затем полагается на поставщиков услуг, чтобы при необходимости его очистить. Поставщики услуг могут очистить и сбросить флаг, вызвав метод **IMAPIProgress:: SetLimits** . Дополнительные сведения о том, как реализовать **Флаги** и другие методы **IMAPIProgress** , приведены в разделе [Реализация индикатора хода выполнения](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При отображении индикатора хода выполнения первым вызывается вызов **IMAPIProgress:: @ flags**. Возвращаемое значение должно быть MAPI_TOP_LEVEL, так как все реализации инициализируют содержимое параметра _лпулфлагс_ значением. Дополнительные сведения о последовательности вызовов для объекта Progress приведены в разделе [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |Кмапипрогресс:: @ flags  <br/> |MFCMAPI использует метод **IMAPIProgress::** ' для определения устанавливаемых флагов. Возвращает MAPI_TOP_LEVEL, если флаги не заданы с помощью метода **IMAPIProgress:: SetLimits** .  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатора хода выполнения](implementing-a-progress-indicator.md)

