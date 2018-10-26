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
ms.openlocfilehash: 32174e213334d784220b960364443e60db6d1d19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582779"
---
# <a name="imapisupportdoprogressdialog"></a>IMAPISupport::DoProgressDialog

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Дескриптор родительского окна индикатор хода выполнения.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который управляет расчет хода выполнения, в объекте хода выполнения. Можно задать следующий флаг:
    
MAPI_TOP_LEVEL 
  
> Ход выполнения рассчитывается для элемент верхнего уровня, например родительской папки. Объект хода выполнения следует использовать значения в параметры метода [IMAPIProgress::Progress](imapiprogress-progress.md) _инициализирует метод ulCount_ и _ulTotal_ — указывающие текущего элемента и итоговых значений в операции, соответственно — для увеличения хода выполнения обновления индикатор для операции. 
    
 _lppProgress_
  
> [out] Указатель на указатель на объект хода выполнения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Ход выполнения объект был успешно извлечен.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::DoProgressDialog** реализуется для адресной книги и сообщения хранилища поставщика объекты поддержки. Эти поставщики вызов **DoProgressDialog** для доступа к MAPI реализации интерфейса [IMAPIProgress](imapiprogressiunknown.md) , которая вычисляет сведения о ходе выполнения и отображает стандартное диалоговое окно. 
  
Для получения сведений об использовании объекта хода выполнения и интерфейс **IMAPIProgress** просмотрите [представление индикатор хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="see-also"></a>См. также



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)

