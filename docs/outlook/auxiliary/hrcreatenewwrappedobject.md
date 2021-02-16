---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Создает объект, к который клиент может получить доступ в предпочитаемом формате символов.
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317607"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

Создает объект, к который клиент может получить доступ в предпочитаемом формате символов.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортируется с помощью:  <br/> |msmapi32.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
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

_pvUnwrapped_
  
> [in] Начальный нерасхваченный объект Outlook. Необходимо реализовать один из следующих интерфейсов:
    
   - [IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), или [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).
    
_ulUnwrappedFlags_
  
> [in] Флаги, которые характеризуют начальный объект без разметки. Должно иметь одно или несколько из следующих значений:
    
   - DDLWRAP_FLAG_ANSI — нерасхваченный объект ANSI.
    
   - DDLWRAP_FLAG_UNICODE — unwrapped object is UNICODE.
    
_ulWrappedFlags_
  
>  [in] Флаги для предпочтительного формата символов. Должно иметь одно или несколько из следующих значений: 
    
   - DDLWRAP_FLAG_ANSI — объект Wrapped будет выставиться как ANSI.
    
   - DDLWRAP_FLAG_UNICODE — объект Wrapped будет иметь ЮНИКОД.
    
_pIID_
  
>  [in] Идентификатор интерфейса, поддерживаемого неподтверченным объектом; установите для него NULL, если это неизвестно. 
    
_pulReserved_
  
>  [in] Этот параметр не используется. Он должен иметь NULL. 
    
_fCheckWrap_
  
>  [in] Установите для этого **параметра true,** если необходимо проверить  _формат pvUnwrapped_ перед переносом; установите для объекта **false,** если объект должен быть оболочкой без проверки. 
    
_ppvWrapped_
  
>  [out] Указатель на запрашиваемой объект, упакованный в запрашиваемом формате символов. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

Передача объекта-оболочки с установленным для  _fCheckWrap_ и true приведет к развертке объекта. Независимо от того, является ли возвращенный объект оболочкой, клиент отвечает за освобождение ссылки на возвращенный объект. 
  
При использовании **GetProcAddress** для искомого адреса этой функции в msmapi32.dll укажите HrCreateNewWrappedObject@28 **в** качестве имени процедуры. 
  
## <a name="see-also"></a>См. также

- [Сведения об API уровня ухудшения данных](about-the-data-degradation-layer-api.md)
- [Константы (API уровня ухудшения данных)](constants-data-degradation-layer-api.md)

