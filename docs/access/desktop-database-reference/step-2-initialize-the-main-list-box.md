---
title: 'Шаг 2: Инициализация главном списке'
TOCTitle: 'Step 2: Initialize the Main List Box'
ms:assetid: 81e4dcfd-6ee0-b5f9-9ea3-026c38c26bf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249562(v=office.15)
ms:contentKeyID: 48545967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2b6b4d79262796aa8e9090d673a439a550f042c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482193"
---
# <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="7436c-102">Шаг 2: Инициализация главном списке</span><span class="sxs-lookup"><span data-stu-id="7436c-102">Step 2: Initialize the Main List Box</span></span>


<span data-ttu-id="7436c-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7436c-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="7436c-104">Шаг 2: Инициализация главном списке</span><span class="sxs-lookup"><span data-stu-id="7436c-104">Step 2: Initialize the Main List Box</span></span>

<span data-ttu-id="7436c-105">**Объявите глобальные объекты набора записей и записи**</span><span class="sxs-lookup"><span data-stu-id="7436c-105">**To declare global Record and Recordset objects**</span></span>

  - <span data-ttu-id="7436c-106">Вставьте следующий код в (Общие) (раздел описаний) для Form1:</span><span class="sxs-lookup"><span data-stu-id="7436c-106">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
    ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
    ```
    
    <span data-ttu-id="7436c-107">Этот код объявляет ссылки на глобальный объект для объектов **записи** и **записей** , которые будут использоваться позже в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="7436c-107">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

<span data-ttu-id="7436c-108">**Чтобы подключиться к URL-адрес и заполнения lstMain**</span><span class="sxs-lookup"><span data-stu-id="7436c-108">**To connect to a URL and populate lstMain**</span></span>

  - <span data-ttu-id="7436c-109">Вставьте следующий код в обработчик событий загрузки формы для Form1:</span><span class="sxs-lookup"><span data-stu-id="7436c-109">Insert the following code into the Form Load event handler for Form1:</span></span>
    
    ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
    ```
    
    <span data-ttu-id="7436c-110">Этот код создает глобальные объекты **набора записей** и **записи** .</span><span class="sxs-lookup"><span data-stu-id="7436c-110">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="7436c-111">**Запись**, grec, открывается с URL-адрес, указанный в качестве **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="7436c-111">The **Record**, grec, is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="7436c-112">Если существует URL-адрес, он открывается; Если он еще не существует, он будет создан.</span><span class="sxs-lookup"><span data-stu-id="7436c-112">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> <span data-ttu-id="7436c-113">Обратите внимание, что необходимо заменить "https://servername/foldername/" с допустимый URL-адрес из среды.</span><span class="sxs-lookup"><span data-stu-id="7436c-113">Note that you should replace "https://servername/foldername/" with a valid URL from your environment.</span></span> <span data-ttu-id="7436c-114">**Набор записей**, grs, открывается на дочерних элементов в **запись**grec.</span><span class="sxs-lookup"><span data-stu-id="7436c-114">The **Recordset**, grs, is opened on the children of the **Record**, grec.</span></span> <span data-ttu-id="7436c-115">Затем lstMain содержит имена файлов ресурсов, опубликованные в URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="7436c-115">Then lstMain is populated with the file names of the resources published to the URL.</span></span>

