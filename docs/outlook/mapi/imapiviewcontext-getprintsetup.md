---
title: Имапивиевконтекстжетпринтсетуп
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351127"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает текущие сведения о печати.
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, определяющих тип возвращаемых строк. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Возвращаемые строки представлены в формате Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.
    
 _Лппформпринтсетуп_
  
> вышли Указатель на структуру, в которой хранятся сведения о печати.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сведения о печати успешно получены.
    
## <a name="remarks"></a>Примечания

Объекты формы вызывают метод **имапивиевконтекст:: жетпринтсетуп** для получения сведений о настройках принтера, прежде чем пытаться напечатать текущее сообщение. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

ВыДеляйте элементы **хдевмоде** и **хдевнаме** структуры [Формпринтсетуп](formprintsetup.md) с помощью функции Win32 **глобалаллок**.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если ожидается, что элементы **хдевмоде** и **хдевнаме** структуры **формпринтсетуп** , на которые указывает параметр _лппформпринтсетуп_ , являются строками в Юникоде, установите _ulFlags_ в мапи_уникоде. В противном случае **жетпринтсетуп** будет возвращать эти строки в формате ANSI. 
  
Освободите члены **хдевмоде** и **хдевнаме** структуры **Формпринтсетуп** , вызвав функцию Win32 **глобалфри**. Освободите всю структуру **формпринтсетуп** , вызвав [мапифрибуффер](mapifreebuffer.md). 
  
## <a name="see-also"></a>См. также



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

