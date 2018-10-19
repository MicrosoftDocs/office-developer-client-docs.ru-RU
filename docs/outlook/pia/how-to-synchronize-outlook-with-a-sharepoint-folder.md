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
# <a name="synchronize-outlook-with-a-sharepoint-folder"></a><span data-ttu-id="62e6e-102">Синхронизация приложения Outlook с папкой SharePoint</span><span class="sxs-lookup"><span data-stu-id="62e6e-102">How to: Synchronize Outlook with a SharePoint Folder</span></span>

<span data-ttu-id="62e6e-103">В этом примере показано, как программным способом подключить Outlook к папке SharePoint и синхронизировать содержимое папки.</span><span class="sxs-lookup"><span data-stu-id="62e6e-103">This example shows how to programmatically connect Outlook with a SharePoint folder and to synchronize the folder contents.</span></span>

## <a name="example"></a><span data-ttu-id="62e6e-104">Пример</span><span class="sxs-lookup"><span data-stu-id="62e6e-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="62e6e-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="62e6e-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="62e6e-106">В Outlook можно синхронизировать с папками SharePoint календари, списки контактов, списки задач, доски обсуждений и библиотеки документов.</span><span class="sxs-lookup"><span data-stu-id="62e6e-106">In Outlook, you can synchronize calendars, contact lists, task lists, discussion boards, and document libraries to SharePoint folders.</span></span> <span data-ttu-id="62e6e-107">На основании предоставленного для синхронизации URL-адреса в приложении Outlook создается новая папка с таким же базовым типом, который имеет папка SharePoint.</span><span class="sxs-lookup"><span data-stu-id="62e6e-107">Based on the URL provided upon synchronization, Outlook will create a new folder of the same base type as the SharePoint folder.</span></span> <span data-ttu-id="62e6e-108">Например, при синхронизации с папкой календаря SharePoint создается новая папка календаря в Outlook.</span><span class="sxs-lookup"><span data-stu-id="62e6e-108">For example, synchronizing to a SharePoint calendar folder will create a new calendar folder in Outlook.</span></span> <span data-ttu-id="62e6e-109">Папки для синхронизации с SharePoint хранятся в собственном файле личных папок Outlook (PST) вне почтового ящика пользователя.</span><span class="sxs-lookup"><span data-stu-id="62e6e-109">SharePoint synchronization folders are stored in their own Outlook Personal Folders (.pst) file outside of the user's mailbox.</span></span> <span data-ttu-id="62e6e-110">К папке SharePoint можно подключиться с помощью метода [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="62e6e-110">You can connect to a SharePoint folder by using the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="62e6e-111">Обратите внимание, что необходимо использовать URL-адрес в формате stssync://, в котором предоставляются сведения о сервере SharePoint, путь к папке и другие данные, необходимые для открытия папки SharePoint в приложении Outlook.</span><span class="sxs-lookup"><span data-stu-id="62e6e-111">Note that you must use a stssync:// URL that provides details about the SharePoint server, folder path, and other information that Outlook needs to open a SharePoint folder.</span></span>

<span data-ttu-id="62e6e-112">При программном подключении к папке SharePoint необходимо определить соответствующий URL-адрес, который будет использоваться для создания отношения совместного доступа.</span><span class="sxs-lookup"><span data-stu-id="62e6e-112">When connecting to a SharePoint folder programmatically, you must determine the proper URL to use to create the sharing relationship.</span></span> <span data-ttu-id="62e6e-113">Так как URL-адрес в формате stssync:// отсутствует в пользовательском интерфейсе SharePoint для папки, следует вручную связать конечную папку с Outlook.</span><span class="sxs-lookup"><span data-stu-id="62e6e-113">Because the stssync:// URL is not provided in the SharePoint user interface for the folder, manually link the destination folder into Outlook.</span></span> <span data-ttu-id="62e6e-114">После этого с помощью первой процедуры следующего примера кода (DisplaySharePointUrl) следует получить соответствующий URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="62e6e-114">Then use the first procedure,  , in the following code example, to get the correct URL.</span></span> <span data-ttu-id="62e6e-115">В процедуре DisplaySharePointUrl используется объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) для поиска сведений о привязке для совместного доступа в текущей папке для активного окна проводника.</span><span class="sxs-lookup"><span data-stu-id="62e6e-115"> uses the Table object to look for the sharing binding information in the current folder for the active explorer window.</span></span> <span data-ttu-id="62e6e-116">Если обнаружен один или нескольких контекстов привязки, отображаются URL-адреса всех имеющихся контекстов общего доступа.</span><span class="sxs-lookup"><span data-stu-id="62e6e-116">If one or more binding contexts are found, the URLs for all available sharing contexts will be displayed.</span></span>

<span data-ttu-id="62e6e-117">Теперь у вас есть соответствующий URL-адрес, чтобы создать отношение совместного доступа.</span><span class="sxs-lookup"><span data-stu-id="62e6e-117">Now you have the proper URL to create the sharing relationship.</span></span> <span data-ttu-id="62e6e-118">Для синхронизации с новой папкой SharePoint в приложении Outlook скопируйте и вставьте этот URL-адрес в качестве значения строковой переменной calendarUrl во второй процедуре (AddSpsFolder).</span><span class="sxs-lookup"><span data-stu-id="62e6e-118">To synchronize the new SharePoint folder in Outlook, copy and paste the URL to the assignment of the string variable   in the second procedure,  .</span></span> <span data-ttu-id="62e6e-119">Процедура AddSpsFolder обеспечивает автоматическую синхронизацию с новой папкой SharePoint в приложении Outlook с помощью метода **NameSpace.OpenSharedFolder**, использующего URL-адрес в формате `stssync://` (в данном случае это URL-адрес, полученный при выполнении процедуры DisplaySharePointUrl).</span><span class="sxs-lookup"><span data-stu-id="62e6e-119"> automates the synchronization of the new SharePoint folder in Outlook by using the NameSpace.OpenSharedFolder method with a stssync:// URL (in this case, the URL produced by the   procedure).</span></span> <span data-ttu-id="62e6e-120">В процедуре AddSpsFolderalso также задается настраиваемое имя папки ("Example SPS Calendar") и использование в Outlook установленного по умолчанию значения срока жизни (TTL).</span><span class="sxs-lookup"><span data-stu-id="62e6e-120">also provides a custom folder name, "Example SPS Calendar", and specifies Outlook to use the default Time to Live (TTL) for the folder.</span></span> <span data-ttu-id="62e6e-121">Папки SharePoint всегда скачивают вложения элементов, поэтому не нужно это указывать здесь.</span><span class="sxs-lookup"><span data-stu-id="62e6e-121">SharePoint folders always download item attachments, so you do not have to specify that here.</span></span>

<span data-ttu-id="62e6e-122">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="62e6e-122">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="62e6e-123">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением public Class.</span><span class="sxs-lookup"><span data-stu-id="62e6e-123">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="62e6e-124">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="62e6e-124">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="62e6e-125">См. также</span><span class="sxs-lookup"><span data-stu-id="62e6e-125">See also</span></span>

- [<span data-ttu-id="62e6e-126">Совместное использование групп</span><span class="sxs-lookup"><span data-stu-id="62e6e-126">Group Sharing</span></span>](group-sharing.md)

