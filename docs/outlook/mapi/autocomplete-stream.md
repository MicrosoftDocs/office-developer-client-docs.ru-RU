---
title: Поток автозаполнения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 7fc1fae4ed648d59c273b20ced247f6d20e01a6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808108"
---
# <a name="autocomplete-stream"></a>Поток автозаполнения

  
  
**Применимо к**: Outlook 
  
В дополнение к информации, как Microsoft Outlook взаимодействует с потоком автозаполнения, необходимо также понять двоичном формате в потоке автозаполнения.
  
Поток автозаполнения представляют собой набор строк получателей свойства, которые сохраняются в виде двоичного потока вместе с некоторые регистрации метаданные, которые используются только в Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 и Microsoft Outlook 2003. Метаданные относится к Outlook взаимодействия с потоком автозаполнения, сторонние производители должны сохранить возможности каждого блока метаданных при сохранении измененного автозаполнения потока. Другими словами сторонние производители следует изменить только часть набор строк двоичного формата и сохранить Какова была уже в блоков метаданных в потоке автозаполнения.
  
## <a name="stream-visualization"></a>Визуализация потока

Общий макет потока автозаполнения выглядит следующим образом:
  
Метаданные (4 байта)
  
Основной номер версии (4 байта)
  
Дополнительный номер версии (4 байта)
  
Количество строк n (4 байта)
  
Число свойств p в первой строке (4 байта)
  
Свойство tag свойство 1 (4 байта)
  
Свойство 1 зарезервировано данных (4 байта)
  
Объединение значение свойства 1 (8 байт)
  
Данные значения свойства 1 (0 или переменной байт)
  
… (свойство 2 через свойство P-1)
  
Тег свойства свойства элемента p (4 байта)
  
P свойства зарезервировано данных (4 байта)
  
Объединение значение свойства элемента p (8 байт)
  
Данные значения свойства элемента p (0 или переменной байт)
  
Число свойств q в двух строк (4 байта)
  
… (строка двух свойств)
  
… (3-n-1 строки строка)
  
Число свойств r в строку n (4 байта)
  
… (строка n's свойств)
  
Дополнительные сведения о число байтов EI (4 байта)
  
Дополнительные сведения о (EI байт)
  
Метаданные (8 байт)
  
В качестве примера двоичной структуры видеть двоичные примера в [Формат файлов Outlook 2003 и 2007 NK2 и рекомендации разработчикам.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
  
## <a name="high-level-layout"></a>Высокоуровневая структура

Вообще, макета в потоке автозаполнения выглядит следующим образом:
  
|**Данные значения**|**Число байт**|
|:-----|:-----|
|Метаданные  <br/> |4  <br/> |
|Основной номер версии  <br/> |4  <br/> |
|Дополнительный номер версии  <br/> |4  <br/> |
|Набор строк  <br/> |Переменная  <br/> |
|Дополнительные сведения о число байтов EI  <br/> |4  <br/> |
|Дополнительные сведения  <br/> |EI  <br/> |
|Метаданные  <br/> |8  <br/> |
   
При чтении этого потока, если основной номер версии, отличается от 12, затем этот поток должен не чтения или записи. Текущий дополнительный номер версии в потоке автозаполнения — 0, который содержит дополнительные сведения о число байтов значение 0. Если дополнительный номер версии, отличается от 0, затем будет сведения в дополнительных сведений, которые необходимо прочитать при чтении потока и сохраняются при записи в поток. Дополнительный номер версии будет также должны сохраняться при записи в поток. Если они не сохраняются, данные будут потеряны экземпляры Outlook, который был создан дополнительных сведений. 
  
> [!NOTE]
> Приложения не следует добавлять пользовательские данные в поле Дополнительные сведения или изменить дополнительный номер версии, как эти функциональные возможности для поддержки расширения Outlook до формата и не произвольных extensions сторонних производителей. 
  
## <a name="row-set-layout"></a>Макет набор строк

Макет набор строк выглядит следующим образом: 
  
|**Данные значения**|**Число байт**|
|:-----|:-----|
|Количество строк  <br/> |4  <br/> |
|Rows  <br/> |Переменная  <br/> |
   
Количество строк определяет, сколько строк поступают в следующей части последовательности двоичного потока.
  
## <a name="row-layout"></a>Макет строк

Каждая строка имеет следующий формат:
  
|**Данные значения**|**Число байт**|
|:-----|:-----|
|Число свойств  <br/> |4  <br/> |
|Свойства  <br/> |Переменная  <br/> |
   
Число свойств определяет, сколько свойства поступают в следующей части последовательности двоичного потока.
  
## <a name="property-layout"></a>Свойство макета

Каждое свойство имеет следующий формат:
  
|**Данные значения**|**Число байт**|
|:-----|:-----|
|Свойство Tag  <br/> |4  <br/> |
|Зарезервированные данных  <br/> |4  <br/> |
|Объединение значение свойства  <br/> ||
|Данные значения  <br/> |0 или переменной (в зависимости от свойства tag)  <br/> |
   
## <a name="interpreting-the-property-value"></a>Интерпретация значения свойства

Объединение значение свойства и значения, воспринимается на основе свойства тега в первые 4 байта в блоке свойство. Этот тег свойства — в виде тега свойства MAPI. Цифры от 0 до 15 тега свойства биты типа свойства. 16 до 31 биты идентификатор свойства. Тип свойства определяет, как следует прочитать остальные свойства.
  
## <a name="static-value"></a>Статическое значение

Некоторые свойства, не имеющие значение данных и только данные в объединение. Следующие типы свойств (которые поступают из свойства Tag) следует воспринимать свойство объединения данных 8 байтов следующим образом:
  
|**Тип свойства**|**Свойство объединения Интерпретация**|
|:-----|:-----|
|PT_I2  <br/> |короткое целое  <br/> |
|PT_LONG  <br/> |длинный  <br/> |
|PT_R4  <br/> |с плавающей запятой  <br/> |
|PT_DOUBLE  <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |короткое целое  <br/> |
|PT_SYSTIME  <br/> |FILETIME  <br/> |
|PT_I8  <br/> |LARGE_INTEGER  <br/> |
   
## <a name="dynamic-values"></a>Динамические значения

Другие свойства содержат данные в блоке значение данных после первого 16 байтов, которые содержат тег свойства, зарезервированные данные и объединения значение свойства. В отличие от статического значения данные, которые хранятся в союзе 8-байтовое значение свойства не имеет значения для чтения. При создании, убедитесь в том, заполните следующие 8 байтов с что-то. Тем не менее содержимое 8 байтов не имеет значения. В динамической значения тип тега свойства определяет, как интерпретировать данные значения.
  
PT_STRING8 
  
|**Данные значения**|**Число байт**|
|:-----|:-----|
|Число байт n  <br/> |4  <br/> |
|Байт в виде строки ANSI (включая символ конца строки)  <br/> |n  <br/> |
   
PT_CLSID
  
|**Данные значения**|**Число байт**|
|:-----|:-----|
|Байт воспринимается как код GUID  <br/> |16  <br/> |
|||
   
PT_BINARY 
  
|**Данные значения**|**Число байт**|
|:-----|:-----|
|Число байт n  <br/> |4  <br/> |
|Байт в виде массива байтов  <br/> |n  <br/> |
   
PT_ERROR
  
|**Данные значения**|**Число байт**|
|:-----|:-----|
|Число байт n  <br/> |4  <br/> |
|Байт в виде массива байтов  <br/> |n  <br/> |
   
PT_MV_BINARY
  
|**Данные значения**|**Число байт**|
|:-----|:-----|
|Количество двоичных массивов X  <br/> |4  <br/> |
|Запустите A байтов, которые содержит X двоичные массивов. Каждый массив интерпретации так же, как запустить PT_BINARY байт.  <br/> |Переменная  <br/> |
   
PT_MV_STRING8 (Outlook 2007, Outlook 2010 и Outlook 2013)
  
|**Данные значения**|**Число байт**|
|:-----|:-----|
|Количество строк ANSI X  <br/> |4  <br/> |
|Запуск байтов, который содержит строки X ANSI. Каждая строка интерпретации так же, как запустить PT_STRING8 байт.  <br/> |Переменная  <br/> |
   
PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)
  
|**Данные значения**|**Число байт**|
|:-----|:-----|
|Количество строк в кодировке Юникод X  <br/> |4  <br/> |
|Запуск байтов, который содержит X UNICODE строк. Каждая строка интерпретации так же, как запустить PT_UNICODE байт.  <br/> |Переменная  <br/> |
   
## <a name="significant-properties"></a>Значительные свойства

Как упоминалось ранее в этом разделе, двоичные блоки, представляющих свойства имеют теги свойства, которые соответствуют свойствам получателей адресной книги. Для свойств, не перечисленных здесь, можно найти в описании свойства в http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx.
  
|**Имя свойства**|**Свойство Tag**|**Описание (Дополнительные сведения см MSDN)**|
|:-----|:-----|:-----|
|PR_NICK_NAME_W (не передаются на получателей, специально для потока автозаполнения только)  <br/> |0x6001001f  <br/> |Это свойство должно быть первым в каждой строке получателя. Функционально служит в качестве идентификатор ключа для строки получателей.  <br/> |
|PR_ENTRYID  <br/> |0x0FFF0102  <br/> |Идентификатор записи книги адрес получателя.  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Отображаемое имя получателя.  <br/> |
|PR_EMAIL_ADDRESS_W  <br/> |0x3003001F  <br/> |Адрес электронной почты получателя (например, johndoe@contoso.com или/o = Contoso/OU = Foo/cn = Recipients/cn = johndoe)  <br/> |
|PR_ADDRTYPE_W  <br/> |0x3002001F  <br/> |Тип адреса получателя (например, SMTP или EX).  <br/> |
|PR_SEARCH_KEY  <br/> |0x300B0102  <br/> |Ключ поиска MAPI получателя.  <br/> |
|PR_SMTP_ADDRESS_W  <br/> |0x39FE001f  <br/> |SMTP-адрес получателя.  <br/> |
|PR_DROPDOWN_DISPLAY_NAME_W (не передаются на получателей, специально для потока автозаполнения только)  <br/> |0X6003001f  <br/> |Строка отображения, который отображается в списке автозаполнения.  <br/> |
|PR_NICK_NAME_WEIGHT (не передаются на получателей, специально для потока автозаполнения только)  <br/> |0x60040003  <br/> |Вес в этой записи автозаполнения. Вес используется для определения, в какой автозаполнения порядке записи возникают при анализе списки автозаполнения. Операции с более высоким вес будут отображаться перед операции с нижней вес. Список завершения автозаполнения сортируется этим свойством. Вес периодически снижает по времени и увеличивается, когда пользователь отправляет сообщение электронной почты данному получателю. В разделе Описание далее в данном разделе приведены дополнительные сведения об этом свойстве.  <br/> |
   
PR_NICK_NAME_WEIGHT
  
Набор строк в потоке автозаполнения сортируются в порядке убывания свойством PR_NICK_NAME_WEIGHT и потока автозаполнения всегда должен сохранить этот отсортированный характеристики. Таким образом любые изменения строки вес необходимо убедиться, что строка содержит порядок сортировки полный набор строк. Любые добавления к набор строк вставляется в правильное положение на обслуживание порядок сортировки.
  
Минимальное значение в этом вес является 0x1 и максимальное значение — LONG_MAX. Все значения для него значение считается недопустимыми.
  
Когда отправляет почты в Outlook 2007 или разрешается получателя, он будет увеличен вес, получатель 0x2000.
  
