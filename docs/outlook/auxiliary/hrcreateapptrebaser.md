---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Инициализирует объект IOlkApptRebaser для использования при повторном Outlook календарях.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317614"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Инициализирует [объект IOlkApptRebaser](iolkapptrebaser.md) для использования при повторном Outlook календарях. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Файл заголовка:  <br/> |tzmovelib.h  <br/> |
|Реализовано в:  <br/> |tzmovelib.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения MAPI  <br/> |
|Тип указателя:  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|Точка входа в DLL:  <br/> |**HrCreateApptRebaser@44** <br/> |
   
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

## <a name="parameters"></a>Parameters

_ulFlags_
  
> [in] Required. Битмаска флагов, используемых для управления тем, как выполняется повторное выполнение. Следующие флаги можно установить и определить в tzmovelib.h:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** — пункты назначения, в которых пользователь является организатором собраний, перебазются. Обратите внимание, что по умолчанию это Outlook отправку обновлений собраний всем участникам любой повторной встречи. Этот флаг можно объединить  с REBASE_FLAG_FORCE_NO_EX_UPDATES **или REBASE_FLAG_FORCE_NO_UPDATES,** чтобы изменить обработку обновлений собраний. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** — обновления элементов назначения, не отмеченных часовой зоной. Если этот флаг задан, значение  *pTZMissing*  используется в качестве часового пояса, в который элемент создается для всех элементов, не имеют данных часового пояса. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** — Обновление только элементов повторяющихся встреч. 
    
   - **REBASE_FLAG_NO_UI** — не отображайте пользовательский интерфейс (пользовательский интерфейс), в том числе диалоговое окно с логотипом, обычно отображаемого при открытии магазина сообщений. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — не перебазить элементы назначения, которые происходят в прошлом. 
    
   - **REBASE_FLAG_FORCE_REBASE** — не проверяйте организатора на повторное принятие решений, а перезамесить пункты назначения, в которых пользователь является пользователем. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** — отправка обновлений только в том случае, если пользователь является организатором, а получатель не подключен к Exchange Server. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** — никогда не отправлять обновления. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** — rebase только одно экземпляра назначения элементов, созданных до исправления был применен. 
    
   - **REBASE_FLAG_REPORTING_MODE** - Не перебазить, просто сообщить о назначениях элементов, которые будут rebased. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** — отправка обновлений собраний в ресурсы. 
    
_pSession_
  
> [in] Required. Указатель на интерфейс сеанса MAPI.
    
_pCalendarMsgStore_
  
> [in] Required. Указатель на хранилище сообщений, содержащий пункты назначения, которые необходимо переназначить.
    
_pCalendarFolder_
  
> [in] Required. Указатель на папку календаря, содержащую пункты назначения, которые необходимо переназначить.
    
_pwszUpdatePrefix_
  
> [in] Optional. Указатель на строку, содержащую префикс, предоплатив для запросов на собрание. Может быть NULL.
    
_pftInstallDateUTC_
  
> [in] Optional. Дата установки патча часовой зоны. Используется только в том **случае, REBASE_FLAG_ONLY_CREATED_PRE_PATCH** установлен флаг. 
    
_IExpansionDepth_
  
> [in] Optional. Глубина расширения при расширении списков рассылки, чтобы исключить получателей, подключенных к Exchange Server. Используется только при **REBASE_FLAG_FORCE_NO_EX_UPDATES** флага. 
    
_pTZTo_
  
> [in] Required. Указатель на структуру **TZDEFINITION,** описывающий часовой пояс, в который необходимо перенастроить. **TZDEFINITION** определяется в tzmovelib. 
    
pTZMissing
  
> [in] Required. Указатель на структуру **TZDEFINITION,** описывающий часовой пояс, который предполагается, если сведения о часовом поясе не штампуются на элементе. Не должен быть NULL, но используется только в том случае, **если REBASE_FLAG_UPDATE_UNMARKED** установлен флаг. 
    
_ppError_
  
> [вышел] Указатель на указатель на структуру **MAPIERROR,** содержащую сведения о версии, компоненте и контексте для ошибки. Может быть NULL, если не требуется расширенных сведений об ошибках. Бесплатно с [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> [вышел] Указатель на указатель на возвращенный **интерфейс IOlkApptRebaser.** 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

При использовании [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) для получения адреса этой функции в  tzmovelib.dll в качестве HrCreateApptRebaser@44 в качестве имени процедуры. Не все флаги действительны в сочетании друг с другом. 
  
Дополнительные сведения о различных вариантах см. в разделе "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

