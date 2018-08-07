---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Создает объект, клиент может получить доступ в предпочтительном символьном формате.
ms.openlocfilehash: 187bcbce8fd1170e05f57c5c9147a8962669fea4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807696"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

Создает объект, клиент может получить доступ в предпочтительном символьном формате.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировать с:  <br/> |Msmapi32.dll  <br/> |
|Вызывается:  <br/> |Клиент  <br/> |
|Реализованный:  <br/> |Outlook  <br/> |
   
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
  
> [in] Начальное развернутый объект Outlook. Должен реализовывать следующие интерфейсы:
    
   - [IMailUser: IMAPIProp](http://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder: IMAPIContainer](http://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage: IMAPIProp](http://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore: IMAPIProp](http://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon: IUnknown](http://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), или [IOSTX](http://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).
    
_ulUnwrappedFlags_
  
> [in] Флаги, создание характеристик развернутый исходный объект. Должен быть один или несколько из следующих значений:
    
   - DDLWRAP_FLAG_ANSI — объект Unwrapped — ANSI.
    
   - DDLWRAP_FLAG_UNICODE — объект Unwrapped — Юникод.
    
_ulWrappedFlags_
  
>  [in] Флаги предпочтительном символьном формате. Должен быть один или несколько из следующих значений: 
    
   - DDLWRAP_FLAG_ANSI — объект Wrapped будут предоставляться как ANSI.
    
   - DDLWRAP_FLAG_UNICODE — объект Wrapped будет предоставлено в качестве Юникод.
    
_pIID_
  
>  [in] Идентификатор элемента интерфейс, поддерживаемый развернутый объект; Задайте его значение NULL, если это не известен. 
    
_pulReserved_
  
>  [in] Этот параметр не используется. Это должен быть NULL. 
    
_fCheckWrap_
  
>  [in] Присвойте этому параметру значение **true** , если _pvUnwrapped_ необходимо проверить его формате перед переносом; Если объект, должны быть помещены без проверки, присвойте этому параметру **значение false** . 
    
_ppvWrapped_
  
>  [out] Указатель на запрошенный объект, заключенное в запрошенные символьном формате. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Remarks

Передача перенесенного объекта с _fCheckWrap_ присвоено **значение true** приведет к развернутый объект. Независимо от того, является ли оформлено возвращенного объекта клиент несет ответственность за освобождение ссылки на возвращенный объект. 
  
При использовании **GetProcAddress** следует искать адреса этой функции msmapi32.dll, укажите **HrCreateNewWrappedObject@28** в качестве имени процедуры. 
  
## <a name="see-also"></a>См. также

- [About the Data Degradation Layer API](about-the-data-degradation-layer-api.md)
- [Константы (layer уменьшение объема данных API).](constants-data-degradation-layer-api.md)

