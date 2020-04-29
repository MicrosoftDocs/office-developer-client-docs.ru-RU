---
title: Каноническое свойство PidLidTimeZoneStruct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346377"
---
# <a name="pidlidtimezonestruct-canonical-property"></a><span data-ttu-id="c5e4e-103">Каноническое свойство PidLidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="c5e4e-103">PidLidTimeZoneStruct Canonical Property</span></span>

  
  
<span data-ttu-id="c5e4e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5e4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5e4e-105">Содержит поток, который сопоставляется с хранимым форматом структуры [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) , который описывает часовой пояс, который будет использоваться для времени начала и окончания повторяющейся встречи или приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="c5e4e-105">Contains a stream that maps to the persisted format of a [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) structure, which describes the time zone to be used for the start and end time of a recurring appointment or meeting request.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5e4e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c5e4e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5e4e-107">диспидтимезонеструкт</span><span class="sxs-lookup"><span data-stu-id="c5e4e-107">dispidTimeZoneStruct</span></span>  <br/> |
|<span data-ttu-id="c5e4e-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c5e4e-108">Property set:</span></span>  <br/> |<span data-ttu-id="c5e4e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="c5e4e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="c5e4e-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="c5e4e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c5e4e-111">0x00008233</span><span class="sxs-lookup"><span data-stu-id="c5e4e-111">0x00008233</span></span>  <br/> |
|<span data-ttu-id="c5e4e-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c5e4e-112">Data type:</span></span>  <br/> |<span data-ttu-id="c5e4e-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c5e4e-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c5e4e-114">Область:</span><span class="sxs-lookup"><span data-stu-id="c5e4e-114">Area:</span></span>  <br/> |<span data-ttu-id="c5e4e-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="c5e4e-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5e4e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5e4e-116">Remarks</span></span>

<span data-ttu-id="c5e4e-117">Microsoft Office Outlook 2003, более ранние версии Outlook и приложения, основанные на объектах данных совместной работы (CDO) 1,21, чьи пользователи не запускают средство обновления календаря, предоставляемое Outlook или Exchange Server, хранят время начала и время окончания встречи или приглашения на собрание как относительное время и сохраняют часовой пояс, в котором создается приглашение на собрание или собрание в **диспидтимезонеструкт**.</span><span class="sxs-lookup"><span data-stu-id="c5e4e-117">Microsoft Office Outlook 2003, earlier versions of Outlook, and applications that are based on Collaboration Data Objects (CDO) 1.21 whose users have not run the calendar update tool provided by Outlook or Exchange Server store the start time and end time of a recurring appointment or meeting request as relative time, and store the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**.</span></span> <span data-ttu-id="c5e4e-118">Тем не менее, эта схема игнорируется, так как правила для часовых поясов могут изменяться, что приводит к изменению некоторых встреч и собраний, которые пользователи запланировали до изменения правил и происходят в неправильное время.</span><span class="sxs-lookup"><span data-stu-id="c5e4e-118">However, this scheme ignores that over time, time zone rules can change, resulting in some appointments and meetings that users scheduled before the rules changed and occur at incorrect times.</span></span> <span data-ttu-id="c5e4e-119">Пользователям и администраторам, не работающим под управлением Windows Vista или не включенных автоматических обновлений, следует использовать инструменты для изменения календарей, которые предоставляются в Outlook или Exchange Server для настройки времени таких встреч и приглашений на собрания.</span><span class="sxs-lookup"><span data-stu-id="c5e4e-119">Users and administrators who are not running Windows Vista or who do not have automatic updates turned on should use the calendar rebasing tools that are provided by Outlook or Exchange Server to adjust the time of such appointments and meeting requests.</span></span> <span data-ttu-id="c5e4e-120">Дополнительные сведения об этих средствах и интерфейсах API для повторного создания календарей в статье сведения о возможностях [перехода на летнее время](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx) в календаре.</span><span class="sxs-lookup"><span data-stu-id="c5e4e-120">For more information about these calendar rebasing tools and APIs that rebase calendars, see [About rebasing calendars programmatically for Daylight Saving Time](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span></span>
  
<span data-ttu-id="c5e4e-121">Используйте следующий формат с прямым порядком байтов при синтаксическом анализе потока, полученного из **диспидтимезонеструкт**, или при сохранении структуры **TZREG** в поток для фиксации в двоичном свойстве **диспидтимезонеструкт** .</span><span class="sxs-lookup"><span data-stu-id="c5e4e-121">Use the following little-endian format when parsing a stream obtained from **dispidTimeZoneStruct**, or when persisting the **TZREG** structure to a stream to commit to the **dispidTimeZoneStruct** binary property.</span></span> 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

<span data-ttu-id="c5e4e-122">Это свойство устанавливается в повторяющихся рядах для указания сведений о часовом поясе, а также указывает способ преобразования полей времени между местным временем и всеобщим скоординированным временем (UTC).</span><span class="sxs-lookup"><span data-stu-id="c5e4e-122">This property is set on a recurring series to specify time-zone information, and specifies how to convert time fields between local time and Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c5e4e-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c5e4e-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c5e4e-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c5e4e-124">Protocol specifications</span></span>

<span data-ttu-id="c5e4e-125">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5e4e-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5e4e-126">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c5e4e-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c5e4e-127">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5e4e-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5e4e-128">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="c5e4e-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c5e4e-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c5e4e-129">Header files</span></span>

<span data-ttu-id="c5e4e-130">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c5e4e-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5e4e-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c5e4e-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5e4e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="c5e4e-132">See also</span></span>



[<span data-ttu-id="c5e4e-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c5e4e-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5e4e-134">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="c5e4e-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5e4e-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c5e4e-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5e4e-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c5e4e-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

