---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Создает объект, к которому клиент может получить доступ в предпочтительном символьном формате.
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317607"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

Создает объект, к которому клиент может получить доступ в предпочтительном символьном формате.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировано:  <br/> |MSMapi32. dll  <br/> |
|Вызывающая сторона:  <br/> |Client  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrCreateNewWrappedObject( 
    LPVOID        pvUnwrapped, 
    ULONG         ulUnwrappedFlags, 
    ULONG         ulWrappedFlags, 
    const IID     *pIID, 
    const ULONG   *pulReserved, 
    BOOL          fCheckWrap, 
    LPVOID       *ppvWrapped 
);

```

## <a name="parameters"></a>Параметры

_пвунвраппед_
  
> возврата Исходный неупакованный объект Outlook. Необходимо реализовать один из следующих интерфейсов:
    
   - [Имаилусер: IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder: IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [iMessage: IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore: IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [имслогон: IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx)или [иосткс](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).
    
_улунвраппедфлагс_
  
> возврата Флаги, характеризующие неупакованный исходный объект. Должно иметь одно или несколько из следующих значений:
    
   - DDLWRAP_FLAG_ANSI — неупакованный объект — ANSI.
    
   - DDLWRAP_FLAG_UNICODE — неупакованный объект — UNICODE.
    
_улвраппедфлагс_
  
>  возврата Флаги для предпочтительного формата знаков. Должно иметь одно или несколько из следующих значений: 
    
   - DDLWRAP_FLAG_ANSI, упакованный объект будет представлен в формате ANSI.
    
   - DDLWRAP_FLAG_UNICODE, упакованный объект будет представлен в формате Юникод.
    
_пиид_
  
>  возврата Идентификатор интерфейса, поддерживаемого неупакованным объектом; Если этот параметр неизвестен, установите для него значение NULL. 
    
_пулресервед_
  
>  возврата Этот параметр не используется. Он должен иметь значение NULL. 
    
_фчеккврап_
  
>  возврата Установите для этого параметра **значение true** , если перед переносом в _пвунвраппед_ необходимо проверить его формат. Задайте для него значение **false** , если объект необходимо включить в оболочку без проверки. 
    
_ппввраппед_
  
>  вышли Указатель на запрошенный объект, заключенный в оболочку запрошенного формата знаков. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

При передаче упакованного объекта с _фчеккврап_ , для которого задано **значение true** , будет получен неупакованный объект. Независимо от того, является ли возвращенный объект упакованным, клиент несет ответственность за освобождение ссылки на возвращенный объект. 
  
При использовании **GetProcAddress** для поиска адреса этой функции в MSMapi32. dll укажите **HrCreateNewWrappedObject@28** в качестве имени процедуры. 
  
## <a name="see-also"></a>См. также

- [Сведения об API уровня ухудшения данных](about-the-data-degradation-layer-api.md)
- [Константы (API уровня замедления данных)](constants-data-degradation-layer-api.md)

