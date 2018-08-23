---
title: Чтение и анализа шаблон повторения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 75113097-b3ae-4d20-9796-85c62a592ef0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5127f5aef50b1040b3e6f4bc644395f2af7555cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563543"
---
# <a name="read-and-parse-a-recurrence-pattern"></a><span data-ttu-id="81994-103">Чтение и анализа шаблон повторения</span><span class="sxs-lookup"><span data-stu-id="81994-103">Read and parse a recurrence pattern</span></span>
  
<span data-ttu-id="81994-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81994-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81994-105">MAPI можно использовать для чтения и анализа шаблона повторения встречи.</span><span class="sxs-lookup"><span data-stu-id="81994-105">MAPI can be used to read and parse a recurrence pattern for an appointment.</span></span>
  
<span data-ttu-id="81994-106">Сведения о загрузке, просмотр и запуск кода из проекта приложения mfcmapi (en), указанного в этом разделе содержатся в разделе [Установка примеров используется в этом разделе](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="81994-106">For information about how to download, view, and run the code from the MFCMAPI application project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-parse-a-recurrence-blob"></a><span data-ttu-id="81994-107">Для анализа большого двоичного объекта повторения</span><span class="sxs-lookup"><span data-stu-id="81994-107">To parse a recurrence blob</span></span>

1. <span data-ttu-id="81994-108">Открытие элемента встречи.</span><span class="sxs-lookup"><span data-stu-id="81994-108">Open an appointment item.</span></span> <span data-ttu-id="81994-109">Сведения об открытии сообщения в разделе [Открытие сообщения](opening-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="81994-109">For information about opening a message, see [Opening a Message](opening-a-message.md).</span></span>
    
2. <span data-ttu-id="81994-110">Получение именованное свойство **dispidApptRecur** ([Каноническое свойство PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="81994-110">Retrieve the named property **dispidApptRecur** ([PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md)).</span></span> <span data-ttu-id="81994-111">Сведения о получении именованных свойств в разделе [Свойства с именем MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="81994-111">For information about retrieving named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span>
    
3. <span data-ttu-id="81994-112">Следуйте указаниям в [[MS-OXOCAL]](http://msdn.microsoft.com/en-us/library/cc425490%28EXCHG.80%29.aspx) для чтения структура шаблона повторения встречи.</span><span class="sxs-lookup"><span data-stu-id="81994-112">Follow the guidance in [[MS-OXOCAL]](http://msdn.microsoft.com/en-us/library/cc425490%28EXCHG.80%29.aspx) to read the appointment recurrence pattern structure.</span></span> 
    
<span data-ttu-id="81994-113">Mfcmapi (en) ссылку приложение демонстрирует последний шаг с `BinToAppointmentRecurrencePatternStruct` функции в исходном файле InterpretProp2.cpp проекта mfcmapi (en).</span><span class="sxs-lookup"><span data-stu-id="81994-113">The MFCMAPI reference application demonstrates the last step with the  `BinToAppointmentRecurrencePatternStruct` function in the InterpretProp2.cpp source file of the MFCMapi project.</span></span> <span data-ttu-id="81994-114">`BinToAppointmentRecurrencePatternStruct` Функция принимает указатель на буфер в памяти как параметр.</span><span class="sxs-lookup"><span data-stu-id="81994-114">The  `BinToAppointmentRecurrencePatternStruct` function takes a pointer to a buffer in memory as a parameter.</span></span> <span data-ttu-id="81994-115">Mfcmapi (en) приложение получит этот буфер сопоставив **dispidApptRecur** именованное свойство для тега свойства, затем, отправив запрос с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) значение свойства.</span><span class="sxs-lookup"><span data-stu-id="81994-115">The MFCMAPI application obtains this buffer by first mapping the **dispidApptRecur** named property to a property tag, then by requesting the property's value using the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="81994-116">Если свойство слишком велик для извлечения с помощью метода **GetProps** , mfcmapi (en) Откроется интерфейс потока, чтобы получить свойство, с помощью метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="81994-116">If the property is too large to retrieve using the **GetProps** method, MFCMAPI opens a stream interface to retrieve the property using the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="81994-117">Затем приложение mfcmapi (en) считывает данные из потока для построения в буфер.</span><span class="sxs-lookup"><span data-stu-id="81994-117">The MFCMAPI application then reads the data out of the stream to build the buffer.</span></span> 
  
<span data-ttu-id="81994-118">Сведения о формате буфера содержатся [Каноническое свойство PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="81994-118">For information about the format of the buffer, see the [PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md).</span></span> <span data-ttu-id="81994-119">Большую часть данных в буфере состоит из полей заданное количество байтов, которые необходимо прочитать поочередно.</span><span class="sxs-lookup"><span data-stu-id="81994-119">The bulk of the data in the buffer consists of fields of a fixed number of bytes, which must be read one after another.</span></span> <span data-ttu-id="81994-120">Некоторые поля присутствуют только в том случае, если другие поля содержат определенные значения и размера в некоторых полях может зависеть от значения других полей.</span><span class="sxs-lookup"><span data-stu-id="81994-120">Some fields are present only if other fields contain certain values, and the size of some fields may depend on the value of other fields.</span></span> <span data-ttu-id="81994-121">Синтаксический анализ буфер для чтения различным полям включает множество регистрации.</span><span class="sxs-lookup"><span data-stu-id="81994-121">Parsing the buffer to read the various fields involves a lot of bookkeeping.</span></span> <span data-ttu-id="81994-122">Mfcmapi (en) с помощью на внутренний вспомогательный класс с именем `CBinaryParser` для инкапсуляции этой регистрации.</span><span class="sxs-lookup"><span data-stu-id="81994-122">MFCMAPI uses an internal helper class named  `CBinaryParser` to encapsulate this bookkeeping.</span></span> <span data-ttu-id="81994-123">Например `CBinaryParser::GetDWORD` функция проверяет ли достаточно байт оставаться в буфер для чтения значение DWORD, считывает значение и обновляет указатели.</span><span class="sxs-lookup"><span data-stu-id="81994-123">For example, the  `CBinaryParser::GetDWORD` function checks whether enough bytes remain in the buffer to read a DWORD, and then reads the value and updates the pointers.</span></span> 
  
<span data-ttu-id="81994-124">После разбора буфера в структуру используется в приложении mfcmapi (en) `AppointmentRecurrencePatternStructToString` функцию, чтобы преобразовать структуру в строку для отображения пользователю.</span><span class="sxs-lookup"><span data-stu-id="81994-124">After the buffer has been parsed into a structure, the MFCMAPI application uses the  `AppointmentRecurrencePatternStructToString` function to convert the structure to a string to display to the user.</span></span> <span data-ttu-id="81994-125">Это не ту же строку Outlook будет отображаться, но вместо этого — это начальное представление данных, для которой Outlook создает логику.</span><span class="sxs-lookup"><span data-stu-id="81994-125">This is not the same string Outlook would display, but is instead a raw view of the data upon which Outlook builds its logic.</span></span> 
  
<span data-ttu-id="81994-126">Существует возможность встретиться буфера, который содержит поврежденных данных или больше данных, чем требуется для кодирования шаблона повторения.</span><span class="sxs-lookup"><span data-stu-id="81994-126">It is possible to encounter a buffer which contains either corrupted data or more data than is needed to encode a recurrence pattern.</span></span> <span data-ttu-id="81994-127">Для определения этих сценариев, приложение mfcmapi (en) отслеживает объем данных успешно проверен и сколько остается в буфер.</span><span class="sxs-lookup"><span data-stu-id="81994-127">To help identify those scenarios, the MFCMAPI application keeps track of how much data has been successfully parsed and how much remains in the buffer.</span></span> <span data-ttu-id="81994-128">Если данные остаются в буфере после завершения синтаксического анализа, mfcmapi (en) включает в себя этот «нежелательных данных» в структуре, может быть проверен.</span><span class="sxs-lookup"><span data-stu-id="81994-128">If data remains in the buffer after parsing has completed, MFCMAPI includes this "junk data" in the structure so it can be examined.</span></span>
  
<span data-ttu-id="81994-129">Ниже приведен полный листинг `BinToAppointmentRecurrencePatternStruct` функции.</span><span class="sxs-lookup"><span data-stu-id="81994-129">The following is the complete listing of the  `BinToAppointmentRecurrencePatternStruct` function.</span></span> 
  
```cpp
AppointmentRecurrencePatternStruct* BinToAppointmentRecurrencePatternStruct(ULONG cbBin, LPBYTE lpBin)
{
   if (!lpBin) return NULL;
   AppointmentRecurrencePatternStruct arpPattern = {0};
   CBinaryParser Parser(cbBin,lpBin);
   size_t cbBinRead = 0;
   arpPattern.RecurrencePattern = BinToRecurrencePatternStruct(cbBin,lpBin,&cbBinRead);
   Parser.Advance(cbBinRead);
   Parser.GetDWORD(&arpPattern.ReaderVersion2);
   Parser.GetDWORD(&arpPattern.WriterVersion2);
   Parser.GetDWORD(&arpPattern.StartTimeOffset);
   Parser.GetDWORD(&arpPattern.EndTimeOffset);
   Parser.GetWORD(&arpPattern.ExceptionCount);
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions)
   {
      arpPattern.ExceptionInfo = new ExceptionInfoStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExceptionInfo)
      {
         memset(arpPattern.ExceptionInfo,0,sizeof(ExceptionInfoStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].StartDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].EndDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].OriginalStartDate);
            Parser.GetWORD(&arpPattern.ExceptionInfo[i].OverrideFlags);
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength2);
               if (arpPattern.ExceptionInfo[i].SubjectLength2 && arpPattern.ExceptionInfo[i].SubjectLength2 + 1 
                  == arpPattern.ExceptionInfo[i].SubjectLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].SubjectLength2,&arpPattern.ExceptionInfo[i].Subject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_MEETINGTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].MeetingType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDERDELTA)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderDelta);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDER)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderSet);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength2);
               if (arpPattern.ExceptionInfo[i].LocationLength2 && arpPattern.ExceptionInfo[i].LocationLength2 
                  + 1 == arpPattern.ExceptionInfo[i].LocationLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].LocationLength2,&arpPattern.ExceptionInfo[i].Location);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_BUSYSTATUS)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].BusyStatus);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_ATTACHMENT)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].Attachment);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].SubType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_APPTCOLOR)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].AppointmentColor);
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock1Size);
   if (arpPattern.ReservedBlock1Size && arpPattern.ReservedBlock1Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock1Size,&arpPattern.ReservedBlock1);
   }
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions &&
      arpPattern.ExceptionInfo)
   {
      arpPattern.ExtendedException = new ExtendedExceptionStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExtendedException)
      {
         memset(arpPattern.ExtendedException,0,sizeof(ExtendedExceptionStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            if (arpPattern.WriterVersion2 >= 0x0003009)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightValue);
               if (arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize > sizeof(DWORD))
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize 
                     - sizeof(DWORD),&arpPattern.ExtendedException[i].ChangeHighlight.Reserved);
               }
            }
            Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE1Size);
            if (arpPattern.ExtendedException[i].ReservedBlockEE1Size &&
                arpPattern.ExtendedException[i].ReservedBlockEE1Size < _MaxReservedBlock)
            {
               Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE1Size,&arpPattern.ExtendedException[i].ReservedBlockEE1);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].StartDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].EndDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].OriginalStartDate);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharSubjectLength);
               if (arpPattern.ExtendedException[i].WideCharSubjectLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharSubjectLength,&arpPattern.ExtendedException[i].WideCharSubject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharLocationLength);
               if (arpPattern.ExtendedException[i].WideCharLocationLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharLocationLength,&arpPattern.ExtendedException[i].WideCharLocation);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE2Size);
               if (arpPattern.ExtendedException[i].ReservedBlockEE2Size && arpPattern.ExtendedException[i].ReservedBlockEE2Size < _MaxReservedBlock)
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE2Size,&arpPattern.ExtendedException[i].ReservedBlockEE2);
               }
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock2Size);
   if (arpPattern.ReservedBlock2Size && arpPattern.ReservedBlock2Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock2Size,&arpPattern.ReservedBlock2);
   }
   // Junk data remains.
   if (Parser.RemainingBytes() > 0)
   {
      arpPattern.JunkDataSize = Parser.RemainingBytes();
      Parser.GetBYTES(arpPattern.JunkDataSize,&arpPattern.JunkData);
   }
   AppointmentRecurrencePatternStruct* parpPattern = new AppointmentRecurrencePatternStruct;
   if (parpPattern)
   {
      *parpPattern = arpPattern;
   }
   return parpPattern;
}

```

## <a name="see-also"></a><span data-ttu-id="81994-130">См. также</span><span class="sxs-lookup"><span data-stu-id="81994-130">See also</span></span>

- [<span data-ttu-id="81994-131">Использование интерфейса MAPI для создания элементов Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="81994-131">Using MAPI to Create Outlook 2007 Items</span></span>](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

