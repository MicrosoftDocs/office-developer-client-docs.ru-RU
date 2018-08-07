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
ms.openlocfilehash: 694d63165bb820ffef1a29d1646861435fc4ed26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808624"
---
# <a name="read-and-parse-a-recurrence-pattern"></a>Чтение и анализа шаблон повторения
  
**Относится к**: Outlook 
  
MAPI можно использовать для чтения и анализа шаблона повторения встречи.
  
Сведения о загрузке, просмотр и запуск кода из проекта приложения mfcmapi (en), указанного в этом разделе содержатся в разделе [Установка примеров используется в этом разделе](how-to-install-the-samples-used-in-this-section.md).

### <a name="to-parse-a-recurrence-blob"></a>Для анализа большого двоичного объекта повторения

1. Открытие элемента встречи. Сведения об открытии сообщения в разделе [Открытие сообщения](opening-a-message.md).
    
2. Получение именованное свойство **dispidApptRecur** ([Каноническое свойство PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)). Сведения о получении именованных свойств в разделе [Свойства с именем MAPI](mapi-named-properties.md).
    
3. Следуйте указаниям в [[MS-OXOCAL]](http://msdn.microsoft.com/en-us/library/cc425490%28EXCHG.80%29.aspx) для чтения структура шаблона повторения встречи. 
    
Mfcmapi (en) ссылку приложение демонстрирует последний шаг с `BinToAppointmentRecurrencePatternStruct` функции в исходном файле InterpretProp2.cpp проекта mfcmapi (en). `BinToAppointmentRecurrencePatternStruct` Функция принимает указатель на буфер в памяти как параметр. Mfcmapi (en) приложение получит этот буфер сопоставив **dispidApptRecur** именованное свойство для тега свойства, затем, отправив запрос с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) значение свойства. Если свойство слишком велик для извлечения с помощью метода **GetProps** , mfcmapi (en) Откроется интерфейс потока, чтобы получить свойство, с помощью метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) . Затем приложение mfcmapi (en) считывает данные из потока для построения в буфер. 
  
Сведения о формате буфера содержатся [Каноническое свойство PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md). Большую часть данных в буфере состоит из полей заданное количество байтов, которые необходимо прочитать поочередно. Некоторые поля присутствуют только в том случае, если другие поля содержат определенные значения и размера в некоторых полях может зависеть от значения других полей. Синтаксический анализ буфер для чтения различным полям включает множество регистрации. Mfcmapi (en) с помощью на внутренний вспомогательный класс с именем `CBinaryParser` для инкапсуляции этой регистрации. Например `CBinaryParser::GetDWORD` функция проверяет ли достаточно байт оставаться в буфер для чтения значение DWORD, считывает значение и обновляет указатели. 
  
После разбора буфера в структуру используется в приложении mfcmapi (en) `AppointmentRecurrencePatternStructToString` функцию, чтобы преобразовать структуру в строку для отображения пользователю. Это не ту же строку Outlook будет отображаться, но вместо этого — это начальное представление данных, для которой Outlook создает логику. 
  
Существует возможность встретиться буфера, который содержит поврежденных данных или больше данных, чем требуется для кодирования шаблона повторения. Для определения этих сценариев, приложение mfcmapi (en) отслеживает объем данных успешно проверен и сколько остается в буфер. Если данные остаются в буфере после завершения синтаксического анализа, mfcmapi (en) включает в себя этот «нежелательных данных» в структуре, может быть проверен.
  
Ниже приведен полный листинг `BinToAppointmentRecurrencePatternStruct` функции. 
  
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

- [Использование интерфейса MAPI для создания элементов Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

