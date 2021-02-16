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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Извлекает объект хода выполнения, который отображает индикатор хода выполнения.
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window of the progress indicator.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет тем, как объект хода выполнения должен вычислять ход выполнения. Можно установить следующий флаг:
    
MAPI_TOP_LEVEL 
  
> Ход выполнения рассчитывается для элемента верхнего уровня, например родительской папки. Объект progress должен использовать значения в параметрах _ulCount_ и _ulTotal_ метода [IMAPIProgress::P gress,](imapiprogress-progress.md) которые указывают текущий элемент и общее число элементов в операции соответственно, для инкремента индикатора хода выполнения операции. 
    
 _lppProgress_
  
> [out] Указатель на указатель на объект хода выполнения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект progress был успешно извлечен.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::D oProgressDialog** реализован для объектов поддержки поставщиков адресной книги и хранения сообщений. Эти поставщики **вызывают DoProgressDialog** для доступа к реализации MAPI [интерфейса IMAPIProgress,](imapiprogressiunknown.md) который вычисляет сведения о ходе выполнения и отображает стандартное диалоговое окно. 
  
Сведения об использовании объекта хода выполнения и **интерфейса IMAPIProgress** см. в подразделе ["Отображение индикатора хода выполнения".](how-to-display-a-progress-indicator.md)
  
## <a name="see-also"></a>См. также



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)

