---
title: Поддержка инструмента iOS Document Picker в Office для iOS
manager: soliver
ms.date: 02/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 802224ef-6eea-4929-824c-507da1c073a5
description: Office для iOS можно интегрировать с инструментом iOS Document Picker с помощью расширения Document Provider, что позволит Office открывать файлы, хранящиеся у другого поставщика документов.
ms.openlocfilehash: e3a3374c7fd33bb00ed076075eb6199c24eec923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299806"
---
# <a name="office-for-ios-support-for-the-ios-document-picker"></a><span data-ttu-id="a7cf1-103">Поддержка инструмента iOS Document Picker в Office для iOS</span><span class="sxs-lookup"><span data-stu-id="a7cf1-103">Office for iOS support for the iOS Document Picker</span></span>

<span data-ttu-id="a7cf1-104">Office для iOS можно интегрировать с инструментом iOS Document Picker с помощью расширения Document Provider, что позволит Office открывать файлы, хранящиеся у другого поставщика документов.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-104">Office for iOS integrates with the iOS Document Picker by means of the Document Provider extension, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="a7cf1-p101">Версии ОС iOS от компании Apple, начиная с iOS 8.0, предусматривают [поддержку расширений приложений](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1). Вы можете использовать эти расширения, чтобы интегрировать функции своего приложения в другие приложения или среды на устройстве пользователя. Чтобы интегрировать Office для iOS и инструмент iOS Document Picker, используйте [расширение Document Provider](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).</span><span class="sxs-lookup"><span data-stu-id="a7cf1-p101">Versions of the Apple iOS starting with iOS 8.0 include [app extension support](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1). You can use these extensions to expand the functionality of your application into other apps or contexts on the user's device. To integrate Office for iOS with the iOS Document Picker, you use the [Document Provider extension](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).</span></span>
  
<span data-ttu-id="a7cf1-108">Расширение Document Provider поддерживает четыре операции:</span><span class="sxs-lookup"><span data-stu-id="a7cf1-108">The Document Provider extension supports four operations:</span></span>
  
- <span data-ttu-id="a7cf1-109">Импорт</span><span class="sxs-lookup"><span data-stu-id="a7cf1-109">Import</span></span>
    
- <span data-ttu-id="a7cf1-110">Экспорт</span><span class="sxs-lookup"><span data-stu-id="a7cf1-110">Export</span></span>
    
- <span data-ttu-id="a7cf1-111">Открытие</span><span class="sxs-lookup"><span data-stu-id="a7cf1-111">Open</span></span>
    
- <span data-ttu-id="a7cf1-112">Перемещение</span><span class="sxs-lookup"><span data-stu-id="a7cf1-112">Move</span></span>
    
<span data-ttu-id="a7cf1-p102">При интеграции Office для iOS доступна операция открытия. После создания расширения Document Provider пользователи могут использовать инструмент Document Picker, чтобы открывать и редактировать документы непосредственно в Office, не создавая копию файла.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-p102">Office for iOS integrates with the open operation. When you create a Document Provider extension, your users can use the Document Picker to open and edit documents directly in Office without creating a duplicate copy of the file.</span></span>
  
## <a name="learn-more-about-app-extensions-and-the-document-picker"></a><span data-ttu-id="a7cf1-115">Дополнительные сведения о расширениях приложений и инструменте Document Picker</span><span class="sxs-lookup"><span data-stu-id="a7cf1-115">Learn more about app extensions and the Document Picker</span></span>
<span data-ttu-id="a7cf1-116"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="a7cf1-116"></span></span>

- [<span data-ttu-id="a7cf1-117">Расширения приложений</span><span class="sxs-lookup"><span data-stu-id="a7cf1-117">App extensions</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
    
- [<span data-ttu-id="a7cf1-118">Руководство по программированию, касающееся Document Picker</span><span class="sxs-lookup"><span data-stu-id="a7cf1-118">Document Picker Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html)
    
- [<span data-ttu-id="a7cf1-119">Руководство по программированию, касающееся Document Provider</span><span class="sxs-lookup"><span data-stu-id="a7cf1-119">Document Provider Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
    

