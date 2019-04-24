---
title: FORMPRINTSETUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FORMPRINTSETUP
api_type:
- COM
ms.assetid: 6e82fe94-47bd-4a25-b25b-0ab6fe2db274
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c2b9176e21341ef28e6f0bc007757b097a05daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327288"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает сведения о настройке печати для объекта Form. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиформ. h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulFlags;
  HDEVMODE hDevMode;
  HDEVNAMES hDevNames;
  ULONG ulFirstPageNumber;
  ULONG ulFPrintAttachments;
} FORMPRINTSETUP, FAR * LPFORMPRINTSETUP;

```

## <a name="members"></a>Элементы

 **ulFlags**
  
> Битовая маска флагов, определяющих тип строк. Можно использовать следующий флаг:
    
MAPI_UNICODE 
  
> Строки представлены в формате Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.
    
 **Хдевмоде**
  
> Режим обработки принтера.
    
 **Хдевнамес**
  
> Ссылка на путь к принтеру.
    
 **Улфирстпаженумбер**
  
> Номер первой страницы, которую необходимо напечатать.
    
 **Улфпринтаттачментс**
  
> Флаг, указывающий на наличие вложений для печати. При наличии вложений для печати для элемента **улфпринтаттачментс** устанавливается значение 1. Если для печати нет вложений, для него задается значение 0. 
    
## <a name="remarks"></a>Замечания

Структура **формпринтсетуп** используется для описания сведений о настройке печати для объекта Form. Реализации [имапивиевконтекст:: жетпринтсетуп](imapiviewcontext-getprintsetup.md) заполните структуру **формпринтсетуп** и верните ее в содержимое выходного параметра _лппформпринтсетуп_ объекта **жетпринтсетуп**.
  
Если в параметре _ulFlags_ объекта **жетпринтсетуп**передается флаг мапи_уникоде, то строки, на которые ссылаются члены **хдевмоде** и **хдевнамес** , должны быть в формате Юникод. В противном случае строки должны быть в формате ANSI. 
  
Средства просмотра форм, реализующие **имапивиевконтекст** , должны выделить структуру **формпринтсетуп** с помощью функции распределителя MAPI [мапиаллокатебуффер](mapiallocatebuffer.md), но выделить отдельные элементы, **хдевмоде** и **хдевнамес**, с помощью функции Windows [глобалаллок](https://go.microsoft.com/fwlink/?LinkId=132110). Аналогичный выпуск памяти обрабатывается аналогично. Члены **хдевмоде** и **хдевнамес** должны быть освобождены с помощью функции Windows [Глобалфри](https://go.microsoft.com/fwlink/?LinkId=132108) , тогда как структура **формпринтсетуп** должна быть освобождена с помощью функции [мапифрибуффер](mapifreebuffer.md) . 
  
## <a name="see-also"></a>См. также



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[Структуры MAPI](mapi-structures.md)

