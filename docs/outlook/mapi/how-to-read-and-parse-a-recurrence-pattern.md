---
title: Чтение и анализ расписания повторения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 75113097-b3ae-4d20-9796-85c62a592ef0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c226fe79fd002cda3c557fc8416c25f98ad33626
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345929"
---
# <a name="read-and-parse-a-recurrence-pattern"></a>Чтение и анализ расписания повторения
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
MAPI можно использовать для чтения и разлиения шаблона повторения встречи.
  
Сведения о загрузке, просмотре и запуске кода из проекта приложения MFCMAPI, на который ссылается этот раздел, см. в разделе "Установка примеров, используемых [в этом разделе".](how-to-install-the-samples-used-in-this-section.md)

### <a name="to-parse-a-recurrence-blob"></a>Разбиение BLOB-ля повторения

1. Откройте элемент встречи. Сведения об открытии сообщения см. в [открываемом сообщении.](opening-a-message.md)
    
2. Получить именованное **свойство dispidApptRecur** ([PidLidAppointmentRecur Canonical Property).](pidlidappointmentrecur-canonical-property.md) Сведения о том, как получить именуемые свойства, см. в под названием [MAPI.](mapi-named-properties.md)
    
3. Следуйте указаниям [в [MS-OXOCAL],](https://msdn.microsoft.com/library/cc425490%28EXCHG.80%29.aspx) чтобы прочитать структуру шаблона повторения встречи. 
    
Справочные приложения MFCMAPI демонстрируют последний шаг с функцией в исходный файл  `BinToAppointmentRecurrencePatternStruct` InterpretProp2.cpp проекта MFCMapi. Функция  `BinToAppointmentRecurrencePatternStruct` принимает указатель на буфер в памяти в качестве параметра. Приложение MFCMAPI получает этот буфер, сначала сопописав именуемого свойства **dispidApptRecur** с тегом свойства, а затем запросив значение свойства с помощью метода [IMAPIProp::GetProps.](imapiprop-getprops.md) Если свойство слишком большое для извлечения с помощью метода **GetProps,** MFCMAPI открывает интерфейс потока для извлечения свойства с помощью метода [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) Затем приложение MFCMAPI считыет данные из потока для построения буфера. 
  
Сведения о формате буфера см. в каноническом свойстве [PidLidAppointmentRecur.](pidlidappointmentrecur-canonical-property.md) Основная часть данных в буфере состоит из полей фиксированного количества вбайт, которые должны читаться друг за другом. Некоторые поля присутствуют только в том случае, если другие поля содержат определенные значения, а размер некоторых полей может зависеть от значения других полей. Разбиение буфера на чтение различных полей требует большой регистрации. MFCMAPI использует внутренний дополнительный класс с  `CBinaryParser` инкапсуляциями этой регистрации. Например, функция проверяет, остается ли в буфере достаточное количество данных для чтения DWORD, а затем считывает значение и обновляет  `CBinaryParser::GetDWORD` указатели. 
  
После разбиение буфера на структуру приложение MFCMAPI использует функцию для преобразования структуры в строку для отображения  `AppointmentRecurrencePatternStructToString` пользователю. Это не та же строка, которую отображает Outlook, а необработанные представления данных, на основе которых Outlook создает свою логику. 
  
Можно столкнуться с буфером, содержащим поврежденные данные или больше данных, чем требуется для кодирования расшифровки расшифровки. Чтобы определить эти сценарии, приложение MFCMAPI отслеживает, какой объем данных был успешно анализировали и сколько осталось в буфере. Если данные остаются в буфере после завершения анализа, MFCMAPI включает эти "нежелательные данные" в структуру для проверки.
  
Ниже приводится полный список  `BinToAppointmentRecurrencePatternStruct` функции. 
  
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

## <a name="see-also"></a>См. также

- [Использование MAPI для создания элементов Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

