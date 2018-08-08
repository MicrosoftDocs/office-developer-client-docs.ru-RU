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
ms.openlocfilehash: a1a96cdb3aed03b9621097f1ef858a09391c0693
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810623"
---
# <a name="pidlidtimezonestruct-canonical-property"></a><span data-ttu-id="55d71-103">Каноническое свойство PidLidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="55d71-103">PidLidTimeZoneStruct Canonical Property</span></span>

  
  
<span data-ttu-id="55d71-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="55d71-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="55d71-105">Содержит поток, который соответствует сохраненного формата структуры [TZREG](http://msdn.microsoft.com/en-us/library/bb820983%28v=office.12%29.aspx) , который описывает часовой пояс, который будет использоваться для времени начала и окончания повторяющейся встречи или приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="55d71-105">Contains a stream that maps to the persisted format of a [TZREG](http://msdn.microsoft.com/en-us/library/bb820983%28v=office.12%29.aspx) structure, which describes the time zone to be used for the start and end time of a recurring appointment or meeting request.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="55d71-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="55d71-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55d71-107">dispidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="55d71-107">dispidTimeZoneStruct</span></span>  <br/> |
|<span data-ttu-id="55d71-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="55d71-108">Property set:</span></span>  <br/> |<span data-ttu-id="55d71-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="55d71-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="55d71-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="55d71-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="55d71-111">0x00008233</span><span class="sxs-lookup"><span data-stu-id="55d71-111">0x00008233</span></span>  <br/> |
|<span data-ttu-id="55d71-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="55d71-112">Data type:</span></span>  <br/> |<span data-ttu-id="55d71-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="55d71-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="55d71-114">Область:</span><span class="sxs-lookup"><span data-stu-id="55d71-114">Area:</span></span>  <br/> |<span data-ttu-id="55d71-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="55d71-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55d71-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="55d71-116">Remarks</span></span>

<span data-ttu-id="55d71-117">Microsoft Office Outlook 2003 более ранних версий Outlook и приложения, основанные на объекты совместной работы (CDO) 1.21, пользователи не запущен средства обновления календаря, реализованного в Outlook или Exchange Server хранить время начала и время окончания повторяющиеся встречи или приглашения на собрание как относительное время и сохранить часовой пояс, в котором создается встречи или приглашения на собрание в **dispidTimeZoneStruct**.</span><span class="sxs-lookup"><span data-stu-id="55d71-117">Microsoft Office Outlook 2003, earlier versions of Outlook, and applications that are based on Collaboration Data Objects (CDO) 1.21 whose users have not run the calendar update tool provided by Outlook or Exchange Server store the start time and end time of a recurring appointment or meeting request as relative time, and store the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**.</span></span> <span data-ttu-id="55d71-118">Тем не менее эта схема игнорирует, что со временем часового пояса правил можно изменить, в результате чего некоторые встречи и собрания, которое пользователи, назначенные перед правила изменено и появляться в неправильные время.</span><span class="sxs-lookup"><span data-stu-id="55d71-118">However, this scheme ignores that over time, time zone rules can change, resulting in some appointments and meetings that users scheduled before the rules changed and occur at incorrect times.</span></span> <span data-ttu-id="55d71-119">Пользователям и администраторам которых не установлена ОС Windows Vista или пользователей, которые не имеют включено автоматическое обновление следует использовать календарь, повторного размещения en средств, предоставляемых Outlook или Exchange Server, чтобы настроить время таких встречи и приглашения на собрания.</span><span class="sxs-lookup"><span data-stu-id="55d71-119">Users and administrators who are not running Windows Vista or who do not have automatic updates turned on should use the calendar rebasing tools that are provided by Outlook or Exchange Server to adjust the time of such appointments and meeting requests.</span></span> <span data-ttu-id="55d71-120">Дополнительные сведения об этих средств сдвига календаря и API, которые перебазирование календарей в разделе [о сдвига календарей программными средствами на летнее время](http://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55d71-120">For more information about these calendar rebasing tools and APIs that rebase calendars, see [About rebasing calendars programmatically for Daylight Saving Time](http://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span></span>
  
<span data-ttu-id="55d71-121">Используйте следующий формат обратным при анализе потока, полученный из **dispidTimeZoneStruct**или при сохранении в структуре **TZREG** для потока, чтобы зафиксировать двоичного свойства **dispidTimeZoneStruct** .</span><span class="sxs-lookup"><span data-stu-id="55d71-121">Use the following little-endian format when parsing a stream obtained from **dispidTimeZoneStruct**, or when persisting the **TZREG** structure to a stream to commit to the **dispidTimeZoneStruct** binary property.</span></span> 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

<span data-ttu-id="55d71-122">Это свойство имеет значение на серии повторяющихся указать часовой пояс сведения и указывает, как преобразовать поля времени между местного времени и времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="55d71-122">This property is set on a recurring series to specify time-zone information, and specifies how to convert time fields between local time and Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="55d71-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="55d71-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55d71-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="55d71-124">Protocol specifications</span></span>

<span data-ttu-id="55d71-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55d71-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55d71-126">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="55d71-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55d71-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55d71-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55d71-128">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="55d71-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55d71-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="55d71-129">Header files</span></span>

<span data-ttu-id="55d71-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55d71-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="55d71-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="55d71-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55d71-132">См. также</span><span class="sxs-lookup"><span data-stu-id="55d71-132">See also</span></span>



[<span data-ttu-id="55d71-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="55d71-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55d71-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="55d71-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55d71-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="55d71-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55d71-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="55d71-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

