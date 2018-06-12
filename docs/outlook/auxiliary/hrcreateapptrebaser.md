---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Инициализирует объект IOlkApptRebaser для использования в модификации базового адреса встреч в календарях Outlook.
ms.openlocfilehash: fec0407c3f129290d03f9b26b0b3f072a229b003
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807707"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Инициализирует объект [IOlkApptRebaser](iolkapptrebaser.md) для использования в модификации базового адреса встреч в календарях Outlook. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Файл заголовка:  <br/> |tzmovelib.h  <br/> |
|Реализованный:  <br/> |tzmovelib.dll  <br/> |
|Вызывается:  <br/> |Клиентские приложения MAPI  <br/> |
|Тип указателя:  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|Точку входа:  <br/> |**HrCreateApptRebaser@44** <br/> |
   
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

## <a name="parameters"></a>���������

_ulFlags_
  
> [in] Required. Битовая маска флаги, используемые для управления, как выполняется изменен базовый адрес. Следующие флаги можно задать и определяются в tzmovelib.h:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** — преобразовываются элементы встречи, в которых пользователь является организатором собрания. Обратите внимание, что по умолчанию, в результате Outlook для отправки обновлений собрания всем участникам собрания, любые модификации. Этот флаг можно объединить с **REBASE_FLAG_FORCE_NO_EX_UPDATES** или **REBASE_FLAG_FORCE_NO_UPDATES** , чтобы изменить порядок обработки обновлений встреч. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** — обновление элементов встречи, которые не были помечены часового пояса. Если этот флаг указан, значение *pTZMissing* используется как часовой пояс, создавшего элемент всех элементов, у которых нет данных часового пояса. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** — обновление только повторяющихся элементов встречи. 
    
   - **REBASE_FLAG_NO_UI** — без отображения пользовательского интерфейса (UI), включая диалоговые окна входа в систему, обычно отображается при открытии хранилища сообщений. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — не Смена базы элементы встреч, которые происходят в прошлом. 
    
   - **REBASE_FLAG_FORCE_REBASE** — не проверять Организатор для повторного размещения en решения, но Смена базы элементы встречи, в которых является пользователь. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** — отправить обновляет только в том случае, если пользователь является организатором и получатель не подключен к серверу Exchange. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** — никогда не отправлять обновления. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** — Перебазировка только элементы единичных встреч, созданные до исправления. 
    
   - **REBASE_FLAG_REPORTING_MODE** — фактически не rebase, только отчет о встрече элементы, может быть модификации базового адреса. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** — отправка обновлений встреч ресурсам. 
    
_pSession_
  
> [in] Required. Указатель на интерфейс сеанса MAPI.
    
_pCalendarMsgStore_
  
> [in] Required. Указатель на сообщение хранилища, содержащего элементы встреч, чтобы быть модификации базового адреса.
    
_pCalendarFolder_
  
> [in] Required. Указатель на папку календаря, содержащую элементы встреч, чтобы быть модификации базового адреса.
    
_pwszUpdatePrefix_
  
> [in] Optional. Указатель на строку, содержащую префикс, которые должны добавляться в начало на приглашений на собрания. Может быть NULL.
    
_pftInstallDateUTC_
  
> [in] Optional. Дата установки исправления часового пояса. Используется только в том случае, если установлен флаг **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** . 
    
_IExpansionDepth_
  
> [in] Optional. Глубина расширения при развертывании рассылки список для исключения получателей, подключенных к Exchange Server. Использовать, только если установлен флаг **REBASE_FLAG_FORCE_NO_EX_UPDATES** . 
    
_pTZTo_
  
> [in] Required. Указатель на структуру **TZDEFINITION** , описывающее часовой пояс, который будет базовый адрес которого изменен. **TZDEFINITION** определен в tzmovelib. 
    
pTZMissing
  
> [in] Required. Указатель на структуру **TZDEFINITION** , описывающее часовой пояс, который будет предполагается, что если сведения о часовом поясе не указывается на элемент. Не должно быть значение NULL, но только если установлен флаг **REBASE_FLAG_UPDATE_UNMARKED** . 
    
_ppError_
  
> [out] Указатель на указатель на структуру **MAPIERROR** , содержащий версии, компонент и контекста сведения об ошибке. Может быть NULL, при необходимости не расширенные сведения об ошибке. Бесплатная загрузка с [MAPIFreeBuffer](http://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> [out] Указатель на указатель на возвращенный интерфейс **IOlkApptRebaser** . 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Remarks

При использовании [GetProcAddress](http://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) следует искать адреса этой функции tzmovelib.dll, укажите **HrCreateApptRebaser@44** в качестве имени процедуры. Не все флаги, допустимый в сочетании друг с другом. 
  
Дополнительные сведения о различных параметрах, обратитесь к разделу «Глоссарий параметров командной строки для средства обновления данных часового пояса Outlook» в [931667 статья БАЗЫ знаний: как часовой пояс изменения адреса с помощью средства обновления данных часового пояса для Microsoft Office Outlook](http://support.microsoft.com/kb/931667/en-us).
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

