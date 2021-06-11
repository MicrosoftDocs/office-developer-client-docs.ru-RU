---
title: IMAPIProgressProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.Progress
api_type:
- COM
ms.assetid: edbf7623-a64e-43b8-8379-e3cde2433d91
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3cf639286a504b9edb600214d13dbe50710e76a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435497"
---
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Обновляет индикатор прогресса с отображением прогресса по мере выполнения операции. 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>Parameters

 _ulValue_
  
> [in] Число, которое указывает текущий уровень прогресса (вычисляется из _параметров ulCount_ и _ulTotal_ или _lpulMin и lpulMax_ метода [IMAPIProgress::SetLimits)](imapiprogress-setlimits.md) между глобальным нижним пределом и глобальным верхним пределом.  
    
 _ulCount_
  
> [in] Число, которое указывает обработанный в настоящее время элемент относительно общего числа.
    
 _ulTotal_
  
> [in] Общее количество элементов, обрабатываемых во время операции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Индикатор прогресса был успешно обновлен.
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Параметр  _ulValue_ будет равен глобальному минимальному значению только в начале операции и глобальному максимальному значению только по завершении операции. 
  
Если это доступно, используйте  _параметры ulCount_ и  _ulTotal,_ чтобы отобразить необязательные сообщения, такие как "5 элементов, завершенных из 10". Если  _для ulCount_ и  _ulTotal_ установлено 0, определите, следует ли визуально изменять индикатор прогресса. Некоторые поставщики услуг устанавливают эти параметры до 0, чтобы указать, что они обрабатывают подобект, ход которого отслеживается по отношению к родительскому объекту. В этой ситуации имеет смысл изменять дисплей только после того, как родительский объект сообщает о прогрессе. Некоторые поставщики услуг каждый раз передают 0 для этих параметров. 
  
Дополнительные сведения о том, как реализовать **progress** и другие [](implementing-a-progress-indicator.md)методы [IMAPIProgress,](imapiprogressiunknown.md) см. в этой информации.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не все три параметра **IMAPIProgress::P требуются.** Единственным параметром, который требуется, является  _ulValue_, число, которое указывает процент прогресса. Если задат MAPI_TOP_LEVEL, можно также передать количество объектов и общее число объектов. Некоторые реализации используют эти значения для отображения фразы, например "5 элементов, завершенных из 10" с индикатором прогресса. 
  
Если вы копируете все сообщения в одной папке, установите  _ulTotal_ к общему числу копируется сообщений. Если вы копируете папку, установите  _ulTotal_ к числу подстановок в папке. Если скопированная папка не содержит подстановок и только сообщений, установите  _ulTotal_ до 1. 
  
Дополнительные сведения о том, как и когда выполнять вызовы объекта хода выполнения, см. в статье [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::P rogress  <br/> |MFCMAPI использует метод **IMAPIProgress::P rogress** для обновления панели состояния MFCMAPI с текущим процентом прогресса, вычисляемого из  _uValue_ и текущих максимальных и минимальных значений.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатора хода выполнения](implementing-a-progress-indicator.md)

