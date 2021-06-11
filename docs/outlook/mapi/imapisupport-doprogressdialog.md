---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3de29e9af5caa82d2e57c8fcbbdab7d5ddb19dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432585"
---
# <a name="imapisupportdoprogressdialog"></a>IMAPISupport::DoProgressDialog

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает объект progress, отображает индикатор прогресса.
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна индикатора прогресса.
    
 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют, как объект прогресса должен вычислять прогресс. Можно установить следующий флаг:
    
MAPI_TOP_LEVEL 
  
> Прогресс рассчитывается для элемента верхнего уровня, например родительской папки. Объект progress должен использовать значения в параметрах _ulCount_ и _ulTotal_ метода [IMAPIProgress::P gress,](imapiprogress-progress.md) которые указывают текущий элемент и общие элементы в операции соответственно, для приумножение индикатора прогресса для операции. 
    
 _lppProgress_
  
> [вышел] Указатель на указатель на объект progress.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект progress был успешно извлечен.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::D ProgressDialog** реализован для объектов поддержки поставщиков адресной книги и магазина сообщений. Эти поставщики звонят **в DoProgressDialog,** чтобы получить доступ к реализации [MAPI интерфейса IMAPIProgress,](imapiprogressiunknown.md) который вычисляет сведения о ходе выполнения и отображает стандартное диалоговое окно. 
  
Сведения о том, как использовать объект прогресса и интерфейс **IMAPIProgress,** см. в этой [информации.](how-to-display-a-progress-indicator.md)
  
## <a name="see-also"></a>См. также



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)

