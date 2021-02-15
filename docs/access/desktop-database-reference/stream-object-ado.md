---
title: Stream object (ADO)
TOCTitle: Stream object (ADO)
ms:assetid: d49b1514-e0b4-0aca-d5c2-8266f3f4fe65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250065(v=office.15)
ms:contentKeyID: 48547945
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1f6d7e8f64f6b14ea699006fc0461cdf0ded2a06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308486"
---
# <a name="stream-object-ado"></a>Stream object (ADO)


**Область применения**: Access 2013, Office 2013

Представляет поток двоичных данных или текста.

## <a name="remarks"></a>Заметки

В иерархиях с древоструктурами, таких как [](record-object-ado.md) файловая система или почтовая система, запись может иметь двоичный поток битов по умолчанию, связанный с ней, который содержит содержимое файла или сообщения электронной почты. Объект **Stream** можно использовать для управления полями или записями, содержащими эти потоки данных. Объект **Stream** можно получить указанными здесь способами.

  - Из URL-адреса, указывав на объект (обычно файл), содержащий двоичные или текстовые данные. Этот объект может быть простым документом, **объектом Record,** представляющим структурированный документ, или папкой.

  - Открыв объект **Stream по умолчанию, связанный** с **объектом Record.** Вы можете получить поток по умолчанию,  связанный с объектом **Record** при его открытие, чтобы исключить круговой путь только для открытия потока.

  - Путем мгновенного с помощью **объекта Stream.** Эти **объекты Stream** можно использовать для хранения данных в целях вашего приложения. В отличие от **потока,** связанного  с URL-адресом или  потоком записи по **умолчанию,** у мгновенного потока нет связи с исходным по умолчанию.

С помощью методов и свойств объекта **Stream** можно сделать следующее:

  - Откройте объект **Stream** из **записи** или URL-адреса с помощью [метода Open.](open-method-ado-stream.md)

  - **Закроем Stream** с помощью метода [Close.](close-method-ado.md)

  - Ввод данных в поток  с помощью методов [Write](write-method-ado.md) и [WriteText.](writetext-method-ado.md)

  - Чтение данных в **потока** с помощью методов [Read](read-method-ado.md) и [ReadText.](readtext-method-ado.md)

  - Запишите **все данные Stream,** которые остаются в буфере ADO, в объект, на который основан метод [Flush.](flush-method-ado.md)

  - Скопируйте содержимое потока в **другой** **поток** с помощью [метода CopyTo.](copyto-method-ado.md)

  - Управление чтением строк из файла источника с помощью метода [SkipLine](skipline-method-ado.md) и свойства [LineSeparator.](lineseparator-property-ado.md)

  - Определите конец положения потока с помощью свойства [EOS](eos-property-ado.md) и [метода SetEOS.](seteos-method-ado.md)

  - Сохраните и восстановите данные в файлах с помощью методов [SaveToFile](savetofile-method-ado.md) и [LoadFromFile.](loadfromfile-method-ado.md)

  - Укажите набор символов, используемый для хранения **Stream** со [свойством Charset.](charset-property-ado.md)

  - Остановка асинхронной операции **потока** с помощью метода [Cancel.](cancel-method-ado.md)

  - Определите количество в потоковом потоке с **помощью** свойства [Size.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream)

  - Управление текущим положением в **потоке** с помощью [свойства Position.](position-property-ado.md)

  - Определите тип данных в **Stream** со [свойством Type.](type-property-ado-stream.md)

  - Определите текущее состояние **потока (закрытого,** открытого или исполняемого) с помощью [свойства State.](state-property-ado.md)

  - Укажите режим доступа для **Stream со** [свойством Mode.](mode-property-ado.md)

> [!NOTE]
> URL-адреса, использующие схему HTTP, автоматически вызывают поставщика [Microsoft OLE DB для интернет-публикации.](microsoft-ole-db-provider-for-internet-publishing.md) Дополнительные сведения см. в [сведениях об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md)


