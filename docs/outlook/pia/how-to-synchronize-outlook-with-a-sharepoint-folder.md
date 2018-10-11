---
title: Синхронизация приложения Outlook с папкой SharePoint
TOCTitle: Synchronize Outlook with a SharePoint folder
ms:assetid: fecb04ab-39c6-43e1-9a21-12ecb29d94fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424483(v=office.15)
ms:contentKeyID: 55119853
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d7fdf4f6cf9d6d473257d335ce968ce8f518ebe2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407179"
---
# <a name="synchronize-outlook-with-a-sharepoint-folder"></a>Синхронизация приложения Outlook с папкой SharePoint

В этом примере показано, как программным способом подключить Outlook к папке SharePoint и синхронизировать содержимое папки.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

В Outlook можно синхронизировать с папками SharePoint календари, списки контактов, списки задач, доски обсуждений и библиотеки документов. На основании предоставленного для синхронизации URL-адреса в приложении Outlook создается новая папка с таким же базовым типом, который имеет папка SharePoint. Например, при синхронизации с папкой календаря SharePoint создается новая папка календаря в Outlook. Папки для синхронизации с SharePoint хранятся в собственном файле личных папок Outlook (PST) вне почтового ящика пользователя. К папке SharePoint можно подключиться с помощью метода [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). Обратите внимание, что необходимо использовать URL-адрес в формате stssync://, в котором предоставляются сведения о сервере SharePoint, путь к папке и другие данные, необходимые для открытия папки SharePoint в приложении Outlook.

При программном подключении к папке SharePoint необходимо определить соответствующий URL-адрес, который будет использоваться для создания отношения совместного доступа. Так как URL-адрес в формате stssync:// отсутствует в пользовательском интерфейсе SharePoint для папки, следует вручную связать конечную папку в Outlook. После этого с помощью первой процедуры следующего примера кода (DisplaySharePointUrl) следует получить соответствующий URL-адрес. В процедуре DisplaySharePointUrl используется объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) для поиска сведений о привязке для совместного доступа в текущей папке для активного окна проводника. Если обнаружен один или нескольких контекстов привязки, отображаются URL-адреса всех имеющихся контекстов общего доступа.

Теперь у вас есть соответствующий URL-адрес, чтобы создать отношение совместного доступа. Для синхронизации с новой папкой SharePoint в приложении Outlook скопируйте и вставьте этот URL-адрес в оператор присваивания значения строковой переменной calendarUrl во второй процедуре (AddSpsFolder). Процедура AddSpsFolder обеспечивает автоматическую синхронизацию с новой папкой SharePoint в приложении Outlook с помощью метода **NameSpace.OpenSharedFolder**, использующего URL-адрес в формате `stssync://` (в данном случае это URL-адрес, полученный при выполнении процедуры DisplaySharePointUrl). В процедуре AddSpsFolderalso также задается настраиваемое имя папки ("Example SPS Calendar"), а также использование в приложении Outlook установленного по умолчанию значения срока жизни (TTL). Папки SharePoint всегда загружают вложения элементов, поэтому не нужно это указывать здесь.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySharePointUrl()
{
    const string PROP_SYNC_URL = 
        "https://schemas.microsoft.com/mapi/id/{00062040-0000-0000-C000-000000000046}/8A24001E";

    Outlook.Folder folder = Application.ActiveExplorer().CurrentFolder as Outlook.Folder;
    Outlook.Table table = folder.GetTable(Type.Missing, Outlook.OlTableContents.olHiddenItems);
    table.Columns.RemoveAll();
    table.Columns.Add("MessageClass");
    table.Columns.Add(PROP_SYNC_URL);

    StringBuilder sb = new StringBuilder();
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        string msgClass, spsUrl;
        msgClass = row["MessageClass"] as string;
        spsUrl = row[PROP_SYNC_URL] as string;

        if (msgClass == "IPM.Sharing.Binding.In")
        {
            sb.Append(spsUrl);
            sb.Append("\r\n");
        }
    }
    if (sb.Length > 0)
    {
        System.Windows.Forms.MessageBox.Show(
            "The following SharePoint Folder URLs were found:\r\n" + sb.ToString());
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("No SharePoint URLs were found in this folder.");
    }
}

private void AddSpsFolder()
{
    string calendarUrl = "stssync://sts/?ver=1.1&type=calendar&cmd=add-folder&base-url=
        https://example.org/calendar&list-url=/Lists/Calendar/calendar.aspx&guid=&site-name=
        Example%20Site&list-name=Calendar";
    string folderName = "Example SPS Calendar";
    bool useDefaultTTL = true;
    Outlook.Folder calendarFolder =
        Application.Session.OpenSharedFolder(calendarUrl, folderName, Type.Missing, useDefaultTTL) 
        as Outlook.Folder;
    Outlook.Explorer exp =
        Application.Explorers.Add(calendarFolder, Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
    exp.Display();
}
```

## <a name="see-also"></a>См. также

- [Совместное использование групп](group-sharing.md)

