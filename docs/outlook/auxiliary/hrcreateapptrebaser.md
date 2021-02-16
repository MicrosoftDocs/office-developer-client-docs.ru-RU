---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Инициализирует объект IOlkApptRebaser для использования при переоценке встреч в календарях Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317614"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Инициализирует [объект IOlkApptRebaser](iolkapptrebaser.md) для использования при переоценке встреч в календарях Outlook. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Файл заголовка:  <br/> |tzmovelib.h  <br/> |
|Реализовано в:  <br/> |tzmovelib.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения MAPI  <br/> |
|Тип указателя:  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|Точка входа DLL:  <br/> |**HrCreateApptRebaser@44** <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a>Параметры

_ulFlags_
  
> [in] Required. Битоваяmas флагов, используемая для управления выполнением повторного использования. Следующие флаги можно установить и определить в tzmovelib.h:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** — элементы встречи, в которых пользователь является организатором собрания, перенастрояются. Обратите внимание, что по умолчанию outlook отправляет обновления собраний всем участникам перенаправляемого собрания. Вы можете объединить этот флаг с REBASE_FLAG_FORCE_NO_EX_UPDATES **или** **REBASE_FLAG_FORCE_NO_UPDATES,** чтобы изменить лад обработку обновлений собраний. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** — обновление элементов встреч, не помеченных часовой пояс. Если этот флаг указан, значение  *pTZMissing*  используется в качестве часового пояса, в который создается элемент для всех элементов без данных часового пояса. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** — обновляют только элементы повторяющихся встреч. 
    
   - **REBASE_FLAG_NO_UI** — не отображайте пользовательский интерфейс, включая диалоги для логотипа, которые обычно отображаются при открытии магазина сообщений. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — не переназначить элементы встреч, которые происходят в прошлом. 
    
   - **REBASE_FLAG_FORCE_REBASE** — не проверяйте организатора на предмет повторного принятия решений, а перенастройку элементов встреч, в которых пользователь является участником. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** - отправлять обновления, только если пользователь является организатором и получатель не подключен к Exchange Server. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** — никогда не отправлять обновления. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** — повторное базовая база элементов встреч, созданных только для одного экземпляра до того, как исправление было применено. 
    
   - **REBASE_FLAG_REPORTING_MODE** — не перебазделайте, просто делайте отчет об элементе встречи, которые будут перебазданы. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** — отправка обновлений собрания на ресурсы. 
    
_pSession_
  
> [in] Required. Указатель на интерфейс сеанса MAPI.
    
_pCalendarMsgStore_
  
> [in] Required. Указатель на хранилище сообщений, содержащее элементы встречи, которые необходимо переназначить.
    
_pCalendarFolder_
  
> [in] Required. Указатель на папку календаря, содержащую элементы встреч, которые необходимо переназначить.
    
_pwszUpdatePrefix_
  
> [in] Optional. Указатель на строку, содержащую префикс, который должен быть в конце запроса на собрание. Может иметь NULL.
    
_pftInstallDateUTC_
  
> [in] Optional. Дата установки исправления часовой пояса. Используется, только если **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** флага. 
    
_IExpansionDepth_
  
> [in] Optional. Глубина расширения при расширении списков рассылки для исключения получателей, подключенных к Exchange Server. Используется, только если **REBASE_FLAG_FORCE_NO_EX_UPDATES** флага. 
    
_pTZTo_
  
> [in] Required. Указатель на структуру **TZDEFINITION,** описывающий часовой пояс для перенастройки. **TZDEFINITION** определяется в tzmovelib. 
    
pTZMissing
  
> [in] Required. Указатель на структуру **TZDEFINITION,** описывающий часовой пояс, который предполагается использовать, если сведения о часовом поясе не помеются в элементе. Не должно быть NULL, но  используется, только если REBASE_FLAG_UPDATE_UNMARKED флага. 
    
_ppError_
  
> [out] Указатель на указатель на структуру **MAPIERROR,** содержащую сведения о версии, компоненте и контексте для ошибки. Может иметь NULL, если расширенные сведения об ошибке не нужны. Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> [out] Указатель на указатель на возвращенный **интерфейс IOlkApptRebaser.** 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

При использовании [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) для искомого адреса этой функции в tzmovelib.dll укажите HrCreateApptRebaser@44 **в** качестве имени процедуры. Не все флаги допустимы в сочетании друг с другом. 
  
Дополнительные сведения о различных параметрах см. в разделе "Глоссарий параметров командной строки для средства обновления данных часового пояса Outlook" в [KB 931667:](https://support.microsoft.com/kb/931667/en-us)как решить проблему изменения часового пояса с помощью средства обновления часового пояса для Microsoft Office Outlook .
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

