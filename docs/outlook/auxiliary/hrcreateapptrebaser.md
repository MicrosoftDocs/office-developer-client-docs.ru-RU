---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Инициализирует объект Иолкапптребасер для использования в переиндексации встреч в календарях Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317614"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Инициализирует объект [иолкапптребасер](iolkapptrebaser.md) для использования в переиндексации встреч в календарях Outlook. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Файл заголовка:  <br/> |тзмовелиб. h  <br/> |
|Реализовано в:  <br/> |тзмовелиб. dll  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения MAPI  <br/> |
|Тип указателя:  <br/> |**лфркреатеапптребасер** <br/> |
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
  
> [in] Required. Битовая маска флагов, используемых для управления выполнением базового процесса. Следующие флаги можно задать и определить в тзмовелиб. h:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** — элементы встречи, в которых пользователь является организатором собрания. Обратите внимание, что по умолчанию Outlook отправляет обновления собраний всем участникам собрания, для которого выполняется перечисление. Этот флаг можно сочетать с **REBASE_FLAG_FORCE_NO_EX_UPDATES** или **REBASE_FLAG_FORCE_NO_UPDATES** , чтобы изменить способ обработки обновлений собраний. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** — обновление элементов встречи, которые не были помечены с помощью часового пояса. Если этот флаг указан, то значение *птзмиссинг* используется как часовой пояс, в течение которого создается элемент для всех элементов, не имеющих данных о часовых поясах. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** — обновление только повторяющихся элементов встреч. 
    
   - **REBASE_FLAG_NO_UI** — не отображать пользовательский интерфейс, в том числе диалоговые окна входа, которые обычно отображаются при открытии хранилища сообщений. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — не изменяйте базовые элементы встречи, которые происходят в прошлое. 
    
   - **REBASE_FLAG_FORCE_REBASE** — не проверяйте организатора для принятия решений по обновлению, но изменяйте базовые элементы встречи, в которых пользователь является участником. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** — Отправка обновлений только в том случае, если пользователь является организатором, а получатель не подключен к серверу Exchange Server. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** — никогда не отправлять обновления. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** — восстановление только тех элементов встречи с одним экземпляром, созданных до применения исправления. 
    
   - **REBASE_FLAG_REPORTING_MODE** — они не переводятся на основной основе, просто сообщают о встречах, которые будут передаваться в базовый. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** — Отправка обновлений на собрания ресурсам. 
    
_псессион_
  
> [in] Required. Указатель на интерфейс сеанса MAPI.
    
_пкалендармсгсторе_
  
> [in] Required. Указатель на хранилище сообщений, содержащее элементы встреч, которые необходимо перестроить.
    
_пкалендарфолдер_
  
> [in] Required. Указатель на папку календаря, в которой содержатся элементы встречи, которые необходимо перестроить.
    
_пвсзупдатепрефикс_
  
> [in] Optional. Указатель на строку, содержащую префикс, который будет добавлен в начало приглашений на собрание. Может иметь значение NULL.
    
_пфтинсталлдатеутк_
  
> [in] Optional. Дата установки исправления часового пояса. Используется только в том случае, если установлен флаг **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** . 
    
_иекспансиондепс_
  
> [in] Optional. Глубина расширения при расширении списков рассылки для исключения получателей, подключенных к серверу Exchange Server. Используется только в том случае, если установлен флаг **REBASE_FLAG_FORCE_NO_EX_UPDATES** . 
    
_птзто_
  
> [in] Required. Указатель на структуру **TZDEFINITION** , описывающую часовой пояс, в который будет выполняться перечисление. **TZDEFINITION** определяется в тзмовелиб. 
    
птзмиссинг
  
> [in] Required. Указатель на структуру **TZDEFINITION** , описывающую часовой пояс, который предполагается использовать, если сведения о часовом поясе не помечены для элемента. Значение не должно быть равно NULL, но используется только в том случае, если установлен флаг **REBASE_FLAG_UPDATE_UNMARKED** . 
    
_пперрор_
  
> вышли Указатель на указатель на структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки. Может иметь значение NULL, если расширенные сведения об ошибке не требуются. Бесплатно с [мапифрибуффер](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ппапптребасе_
  
> вышли Указатель на указатель на возвращенный интерфейс **иолкапптребасер** . 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

При использовании [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) для поиска адреса этой функции в тзмовелиб. dll укажите **HrCreateApptRebaser@44** в качестве имени процедуры. Не все флаги являются допустимыми в сочетании друг с другом. 
  
Дополнительные сведения о различных параметрах можно найти в разделе "Глоссарий по параметрам командной строки для средства обновления данных о часовых поясах Outlook" в статье [KB 931667: сведения об изменении часового пояса с помощью средства обновления данных часовых поясов для Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

