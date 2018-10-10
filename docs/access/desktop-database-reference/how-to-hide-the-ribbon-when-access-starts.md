---
title: Скрытие ленты при запуске Access
TOCTitle: Hide the ribbon when Access starts
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b2b3e28157662a585fa03353da92a598b96bd2c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480437"
---
# <a name="hide-the-ribbon-when-access-starts"></a>Скрытие ленты при запуске Access

**Применимо к:** Access 2013 | Office 2013

По умолчанию Microsoft Access не предоставляет метод для скрытия на ленте. В этом разделе описывается, как загрузить настраиваемой ленты, который скрывает все встроенной вкладки.

Чтобы загрузить настраиваемой ленты при запуске Access, следует хранить его параметры в таблице с именем **USysRibbons**.

В таблице **USysRibbons** должны быть созданы с помощью имена определенных столбцов в порядке для настройки ленты для реализации. В следующей таблице перечислены параметры для использования при создании в таблице **USysRibbons** .

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя столбца</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>Текст</p></td>
<td><p>Содержит имя настраиваемой ленты, который будет связан с этой настройкой.</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Заметка</p></td>
<td><p>Содержит XML расширяемости ленты (RibbonX), который определяет настройки ленты.</p></td>
</tr>
</tbody>
</table>


В следующей таблице перечислены параметры настройки ленты для хранения в таблице **USysRibbons** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя столбца</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>HideTheRibbon</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;ленты startFromScratch =&quot;значение true,&quot;/&gt;&lt;/CustomUI&gt;</p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a>Применение настраиваемой ленты при запуске Access

Чтобы применить настраиваемой ленты, чтобы оно доступно при запуске приложения, используйте следующую процедуру:

1.  Выполните действия, описанные выше, чтобы сделать доступным для приложения настраиваемой ленты.

2.  Закройте и перезапустите приложение.

3.  Нажмите **Кнопку Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") и нажмите кнопку **Параметры Access**.

4.  Выберите параметр **Текущей базы данных** , а затем, в разделе **ленты и параметры панели инструментов** выберите в списке **Имя ленты** и выберите **HideTheRibbon**.

5.  Закройте и перезапустите приложение.

> [!NOTE]
> Дополнительные сведения о пользовательский Интерфейс ленты в других приложениях Office можно [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


