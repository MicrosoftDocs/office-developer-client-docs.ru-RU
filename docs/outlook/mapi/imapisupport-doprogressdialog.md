---
title: Имаписуппортдопрогрессдиалог
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
  
Получает объект Progress, который отображает индикатор хода выполнения.
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>Параметры

 _Улуипарам_
  
> возврата Дескриптор родительского окна индикатора хода выполнения.
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющих способ вычисления объекта хода выполнения. Можно задать следующий флаг:
    
МАПИ_ТОП_ЛЕВЕЛ 
  
> Ход выполнения вычисляется для элемента верхнего уровня, например для родительской папки. Объект Progress должен использовать значения в параметрах _улкаунт_ и _ултотал_ метода [IMAPIProgress::P рогресс](imapiprogress-progress.md) , которые указывают текущий элемент и общее количество элементов в операции, соответственно, для увеличения хода выполнения индикатор для операции. 
    
 _Лпппрогресс_
  
> вышли Указатель на указатель на объект хода выполнения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект Progress успешно получен.
    
## <a name="remarks"></a>Примечания

Метод **имаписуппорт::D опрогрессдиалог** реализован для адресных книг и объектов поддержки поставщиков хранилища сообщений. Эти поставщики вызывают **допрогрессдиалог** для доступа к реализации MAPI интерфейса [IMAPIProgress](imapiprogressiunknown.md) , который вычисляет сведения о ходе выполнения и отображает стандартное диалоговое окно. 
  
Сведения о том, как использовать объект Progress и интерфейс **IMAPIProgress** , приведены в разделе [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="see-also"></a>См. также



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)

