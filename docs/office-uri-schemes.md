---
title: Схемы URI Office
manager: luken
ms.date: 01/14/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ea99a8f-b005-4b92-b313-923294d20fbf
ms.openlocfilehash: 71325af974e4778d65bea7d74561bde3c9c8bca2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394036"
---
# <a name="office-uri-schemes"></a><span data-ttu-id="f9ff3-102">Схемы URI Office</span><span class="sxs-lookup"><span data-stu-id="f9ff3-102">Office URI Schemes</span></span>

## <a name="11-abstract"></a><span data-ttu-id="f9ff3-103">1.1 СВОДКА</span><span class="sxs-lookup"><span data-stu-id="f9ff3-103">1.1 ABSTRACT</span></span>

<span data-ttu-id="f9ff3-p101">В этом документе определяется формат универсального кода ресурса (URI) для офисных приложений. Эта схема поддерживается в Microsoft Office 2010 с пакетом обновлений 2 (SP2) и более поздних версиях, в том числе в Microsoft Office 2013 для Windows и Microsoft SharePoint 2013. Она также поддерживается в Office для iPhone, Office для iPad и Office для Mac 2011.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p101">This document defines the format of Uniform Resource Identifiers (URIs) for office productivity applications. The scheme is supported in Microsoft Office 2010 Service Pack 2 and later, including the Microsoft Office 2013 for Windows and the Microsoft SharePoint 2013 products. It is also supported in Office for iPhone, Office for iPad, and Office for Mac 2011.</span></span>
  
## <a name="12-introduction"></a><span data-ttu-id="f9ff3-107">1.2 ВВЕДЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9ff3-107">1.2 INTRODUCTION</span></span>

<span data-ttu-id="f9ff3-p102">Эти схемы URI позволяют вызывать офисные приложения различными командами. Каждое приложение получает отдельную именованную схему, но все схемы следуют одним правилам формирования URI (схеме URI).</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p102">These URI schemes allow for office productivity applications to be invoked with various commands. Each application is given a different named scheme but all schemes follow the same rules for how the URI is formed (URI Schema).</span></span>
  
## <a name="13-uri-schema"></a><span data-ttu-id="f9ff3-110">1.3 СХЕМА URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-110">1.3 URI SCHEMA</span></span>

### <a name="full-schema"></a><span data-ttu-id="f9ff3-111">Полная схема</span><span class="sxs-lookup"><span data-stu-id="f9ff3-111">Full schema</span></span>

<span data-ttu-id="f9ff3-112">< *scheme-name*  >:<  *command-name*  >"|"<  *command-argument-descriptor*  > "|"<  *command-argument*  ></span><span class="sxs-lookup"><span data-stu-id="f9ff3-112">< *scheme-name*  >:<  *command-name*  >"|"<  *command-argument-descriptor*  > "|"<  *command-argument*  ></span></span> 
  
<span data-ttu-id="f9ff3-p103">Согласно данному документу URI может содержать один или несколько аргументов команды, каждый из которых должен содержать элементы < *command-argument-descriptor*  > и <  *command-argument*  >, разделенные символом вертикальной черты ("|"). Если в URI несколько аргументов команд, они должны быть разделены вертикальной чертой ("|").</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p103">A URI as defined in this document may have one or more command arguments, each of which must include both the < *command-argument-descriptor*  > and the <  *command-argument*  > elements and be delimited by the vertical bar ("|") character. When more than one command argument is included in a URI there must be a vertical bar ("|") character separating each command argument from the following command argument.</span></span> 
  
<span data-ttu-id="f9ff3-p104">Эти схемы не содержат компонент центра, как определено в разделе 3.2 документа RFC 3986. Вызов команд, указанных в этом документе, происходит в контексте системы, вызывающей команду. Например, если URI "ms-excel:ofv|u|https://contoso/Q4/budget.xls" вызывается с личного компьютера под управлением Microsoft Windows с установленным Microsoft Office 2013, ожидаемым результатом будет запуск локальной установки Microsoft Excel, которой передаются аргументы для открытия файла  *https://contoso/Q4/budget.xls*  в режиме только для чтения. Обратите внимание, что вертикальная черта, используемая как разделитель в этой спецификации, не входит в число символов, определенных в разделе 2.2 документа RFC 3986 как зарезервированные для возможного использования в качестве разделителей. Это сделано специально, чтобы расширить число символов, поддерживаемых аргументами команд URI без их кодирования с использованием символа процента.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p104">These schemes do not include an authority component as defined in section 3.2 of RFC 3986. Invocation of the commands specified in this document takes place in the context of the system invoking the command. For example, when the URI "ms-excel:ofv|u|https://contoso/Q4/budget.xls" is invoked from a personal computer running Microsoft Windows with Microsoft Office 2013 installed the expected result is that the local installation of Microsoft Excel will be launched and passed arguments to open the file at  *https://contoso/Q4/budget.xls*  in read-only mode. Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span> 
  
<span data-ttu-id="f9ff3-120">Синтаксис содержит следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="f9ff3-120">The scheme syntax includes the following:</span></span>
  
1. <span data-ttu-id="f9ff3-p105">< *scheme-name*  >. Это тип вызываемого приложения. Например, имя схемы ms-word: зарегистрировано Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p105">< *scheme-name*  >: This refers to the type of application that should be invoked. For instance, the ms-word: scheme name is registered by Microsoft Word.</span></span> 
    
2. <span data-ttu-id="f9ff3-123">Разделитель ":"</span><span class="sxs-lookup"><span data-stu-id="f9ff3-123">":" separator</span></span>
    
3. <span data-ttu-id="f9ff3-p106">< *command-name*  >. Этот элемент описывает действия, которые должно выполнить приложение, например открыть документ для просмотра. Список имен команд описан в разделе 1.5.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p106">< *command-name*  >: This describes the actions that the application should perform. For instance, opening a document for viewing. The list of command names is described in section 1.5.</span></span> 
    
4. <span data-ttu-id="f9ff3-127">Разделитель "|" (вертикальная черта)</span><span class="sxs-lookup"><span data-stu-id="f9ff3-127">"|" (vertical bar) separator</span></span>
    
5. <span data-ttu-id="f9ff3-128">< *command-argument-descriptor*  >. Этот элемент предоставляет дополнительные сведения об аргументе команды.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-128">< *command-argument-descriptor*  >: This element gives more information about what the command argument is about.</span></span> 
    
6. <span data-ttu-id="f9ff3-129">Разделитель "|" (вертикальная черта)</span><span class="sxs-lookup"><span data-stu-id="f9ff3-129">"|" (vertical bar) separator</span></span>
    
7. <span data-ttu-id="f9ff3-p107">< *command-argument*  >. Аргументы зависят от команды. Общий аргумент  это URI документа, обычно использующий схему http или https. Обратите внимание, что в сегментах <  *command-argument*  > зарезервированные RFC 3986 символы ":" и "/" входят в данные аргумента, а не представляют разделители, поэтому их можно добавлять без экранирования.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p107">< *command-argument*  >: The arguments vary depending on the command. One common argument is the URI to a document, typically using the http or https scheme. Note that within <  *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
    
### <a name="abbreviated-schema"></a><span data-ttu-id="f9ff3-133">Сокращенная схема</span><span class="sxs-lookup"><span data-stu-id="f9ff3-133">Abbreviated schema</span></span>

<span data-ttu-id="f9ff3-p108">Сокращенная форма схем офисных URI позволяет использовать более компактные запросы для запуска указанного приложения Office для открытия ресурса, расположенного по указанному URI. Эта сокращенная форма предполагает, что использует элемент < *command-name*  > "ofv" и элемент <  *command-argument-descriptor*  > "u". Другие команды и аргументы команд для этой схемы не разрешены.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p108">An abbreviated form of the office URI schemes allows for a more compact request to launch a specified Office application to open the resource located at a given URI. This abbreviated form implies the < *command-name*  > "ofv" and the <  *command-argument-descriptor*  > "u". No further commands or command arguments are allowed in this schema.</span></span> 
  
<span data-ttu-id="f9ff3-137">< *scheme-name*  >:<  *command-argument*  ></span><span class="sxs-lookup"><span data-stu-id="f9ff3-137">< *scheme-name*  >:<  *command-argument*  ></span></span> 
  
1. <span data-ttu-id="f9ff3-p109">< *scheme-name*  >: Тип вызываемого приложения. Например, ms-word: для Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p109">< *scheme-name*  >: the type of application that should be invoked. For instance ms-word: for Microsoft Word.</span></span> 
    
2. <span data-ttu-id="f9ff3-p110">< *command-argument*  >. URI ресурса, который должно открыть приложение. В текущий момент поддерживаются только URI на основе схемы http или https.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p110">< *command-argument*  >: URI for the resource the application should open. Currently only URIs based on the http or https scheme are supported.</span></span> 
    
## <a name="14-scheme-names-and-office-application-registrations"></a><span data-ttu-id="f9ff3-142">1.4 ИМЕНА СХЕМ И РЕГИСТРАЦИЯ ПРИЛОЖЕНИЙ OFFICE</span><span class="sxs-lookup"><span data-stu-id="f9ff3-142">1.4 SCHEME NAMES AND OFFICE APPLICATION REGISTRATIONS</span></span>

<span data-ttu-id="f9ff3-p111">Далее представлен список имен схем, реализованных в приложениях Microsoft Office. Если Microsoft Office установлен, имя каждой схемы зарегистрировано в Windows, чтобы их обрабатывал продукт Office с тем же названием. Обратите внимание, что "ms-spd"  это сокращение от SharePoint Designer.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p111">The following is the list of scheme names implemented in Microsoft Office applications. When Microsoft Office is installed, each scheme name is registered with Windows to be handled by the Office product of the same name. Note that "ms-spd" is an abbreviation for SharePoint Designer.</span></span>
  
> - <span data-ttu-id="f9ff3-146">*ms-word:*</span><span class="sxs-lookup"><span data-stu-id="f9ff3-146">*ms-word:*</span></span> 
    
> - <span data-ttu-id="f9ff3-147">*ms-powerpoint:*</span><span class="sxs-lookup"><span data-stu-id="f9ff3-147">*ms-powerpoint:*</span></span> 
    
> - <span data-ttu-id="f9ff3-148">*ms-excel:*</span><span class="sxs-lookup"><span data-stu-id="f9ff3-148">*ms-excel:*</span></span> 
    
> - <span data-ttu-id="f9ff3-149">*ms-visio:*</span><span class="sxs-lookup"><span data-stu-id="f9ff3-149">*ms-visio:*</span></span> 
    
> - <span data-ttu-id="f9ff3-150">*ms-access:*</span><span class="sxs-lookup"><span data-stu-id="f9ff3-150">*ms-access:*</span></span> 
    
> - <span data-ttu-id="f9ff3-151">*ms-project:*</span><span class="sxs-lookup"><span data-stu-id="f9ff3-151">*ms-project:*</span></span> 
    
> - <span data-ttu-id="f9ff3-152">*ms-publisher:*</span><span class="sxs-lookup"><span data-stu-id="f9ff3-152">*ms-publisher:*</span></span> 
    
> - <span data-ttu-id="f9ff3-153">*ms-spd:*</span><span class="sxs-lookup"><span data-stu-id="f9ff3-153">*ms-spd:*</span></span> 
    
> - <span data-ttu-id="f9ff3-154">*ms-infopath:*</span><span class="sxs-lookup"><span data-stu-id="f9ff3-154">*ms-infopath:*</span></span> 
    
## <a name="15-commands-and-required-command-arguments"></a><span data-ttu-id="f9ff3-155">1.5 КОМАНДЫ И ОБЯЗАТЕЛЬНЫЕ АРГУМЕНТЫ КОМАНД</span><span class="sxs-lookup"><span data-stu-id="f9ff3-155">1.5 COMMANDS AND REQUIRED COMMAND ARGUMENTS</span></span>

### <a name="view-document"></a><span data-ttu-id="f9ff3-156">Просмотр документа</span><span class="sxs-lookup"><span data-stu-id="f9ff3-156">View Document</span></span>

<span data-ttu-id="f9ff3-157">Следующая команда приводит к открытию документа, указанного URI, в приложении в режиме только для чтения или просмотра.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-157">The following command will cause the application to open the document referenced by the URI in a read-only or view mode.</span></span>
  
> <span data-ttu-id="f9ff3-158">Имя команды: ofv</span><span class="sxs-lookup"><span data-stu-id="f9ff3-158">Command Name: ofv</span></span>
    
> <span data-ttu-id="f9ff3-159">Дескриптор аргумента команды: u</span><span class="sxs-lookup"><span data-stu-id="f9ff3-159">Command argument descriptor: u</span></span>
    
> <span data-ttu-id="f9ff3-160">Аргумент команды: URI документа на основе схемы http или https</span><span class="sxs-lookup"><span data-stu-id="f9ff3-160">Command argument: a URI to the document, based on the http or https scheme</span></span>
    
> <span data-ttu-id="f9ff3-161">Пример:  *ms-excel:ofv|u|https://contoso/Q4/budget.xls*</span><span class="sxs-lookup"><span data-stu-id="f9ff3-161">Example:  *ms-excel:ofv|u|https://contoso/Q4/budget.xls*</span></span> 
    
### <a name="edit-document"></a><span data-ttu-id="f9ff3-162">Изменить документ</span><span class="sxs-lookup"><span data-stu-id="f9ff3-162">Edit Document</span></span>

<span data-ttu-id="f9ff3-163">Следующая команда приводит к открытию документа, указанного URI, в приложении в режиме редактирования.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-163">The following command will cause the application to open the document referenced by the URI in editing mode.</span></span>
  
> <span data-ttu-id="f9ff3-164">Имя команды: ofe</span><span class="sxs-lookup"><span data-stu-id="f9ff3-164">Command Name: ofe</span></span>
    
> <span data-ttu-id="f9ff3-165">Дескриптор аргумента команды: u</span><span class="sxs-lookup"><span data-stu-id="f9ff3-165">Command argument descriptor: u</span></span>
    
> <span data-ttu-id="f9ff3-166">Аргумент команды: URI документа на основе схемы http или https</span><span class="sxs-lookup"><span data-stu-id="f9ff3-166">Command argument: a URI to the document, based on the http or https scheme</span></span>
    
> <span data-ttu-id="f9ff3-167">Пример:  *ms-powerpoint:ofe|u|https://www.fourthcoffee.com/AllHandsDeck.ppt*</span><span class="sxs-lookup"><span data-stu-id="f9ff3-167">Example:  *ms-powerpoint:ofe|u|https://www.fourthcoffee.com/AllHandsDeck.ppt*</span></span> 
    
### <a name="new-document-from-template"></a><span data-ttu-id="f9ff3-168">Создание документа из шаблона</span><span class="sxs-lookup"><span data-stu-id="f9ff3-168">New Document from Template</span></span>

<span data-ttu-id="f9ff3-p112">Следующая команда приводит к созданию документа в приложении на основе шаблона, хранимого по указанному URI. Файл шаблона в этом процессе не меняется. Можно предоставить дополнительный аргумент команды, чтобы указать путь по умолчанию для первого сохранения файла. Пользователь может выбрать другое расположение.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p112">The following command will cause the application to create and open a new document based on the template stored at the specified URI. The template file is not modified in this process. An additional command argument may be supplied to specify the default path offered as a save location when the file is first saved. It is possible for the user to choose a different location.</span></span>
  
> <span data-ttu-id="f9ff3-173">Имя команды: nft</span><span class="sxs-lookup"><span data-stu-id="f9ff3-173">Command Name: nft</span></span>
    
> <span data-ttu-id="f9ff3-174">Дескриптор аргумента команды 1: u</span><span class="sxs-lookup"><span data-stu-id="f9ff3-174">Command argument descriptor 1: u</span></span>
    
> <span data-ttu-id="f9ff3-175">Аргумент команды 1: URI шаблона на основе схемы http или https</span><span class="sxs-lookup"><span data-stu-id="f9ff3-175">Command argument 1: a URI to the template, based on the http or https scheme</span></span>
    
> <span data-ttu-id="f9ff3-176">Необязательный дескриптор аргумента команды 2: s</span><span class="sxs-lookup"><span data-stu-id="f9ff3-176">Optional Command argument descriptor 2: s</span></span>
    
> <span data-ttu-id="f9ff3-177">Необязательный аргумент команды 2: URI папки сохранения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f9ff3-177">Optional Command argument 2: URI to specify the default save folder</span></span>
    
> <span data-ttu-id="f9ff3-178">Пример:  *ms-word:nft|u|https://cohowinery/templates/elegance.pot|s|https://cohowinery/presentations*</span><span class="sxs-lookup"><span data-stu-id="f9ff3-178">Example:  *ms-word:nft|u|https://cohowinery/templates/elegance.pot|s|https://cohowinery/presentations*</span></span> 
    
<span data-ttu-id="f9ff3-179">Обратите внимание, что если указана необязательная папка для сохранения по умолчанию, она должна указывать на то же имя узла, что и шаблон.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-179">As a note, if the optional default save location is supplied, it must be pointing to the same host name as the template.</span></span>
  
<span data-ttu-id="f9ff3-180">Кроме того, приложения SharePoint Designer и InfoPath (которые реализуют схему ms-spd: и схемы ms-infopath: соответственно) не поддерживают функцию создания документа из шаблона.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-180">Additionally, the SharePoint Designer and InfoPath applications (which implement the ms-spd: scheme and ms-infopath: schemes, respectively) do not support the "new document from template" functionality.</span></span>
  
## <a name="16-backwards-compatibility"></a><span data-ttu-id="f9ff3-181">1.6 ОБРАТНАЯ СОВМЕСТИМОСТЬ</span><span class="sxs-lookup"><span data-stu-id="f9ff3-181">1.6 BACKWARDS COMPATIBILITY</span></span>

<span data-ttu-id="f9ff3-p113">При синтаксическом анализе URI для извлечения соответствующих аргументов данной команды обработчик URI Office будет использовать только аргументы с ожидаемым дескриптором аргумента. Если существуют дополнительные пары аргументов и дескрипторов аргументов с непредвиденными дескрипторами, они будут удалены из URI. Этот механизм позволяет будущим версиям схемы добавлять аргументы команд, не нарушая обратную совместимость с предыдущими реализациями этой схемы.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p113">When parsing a URI to extract the appropriate command arguments for a given command, the Office URI handler will only use the command arguments that have the expected command argument descriptor. If there are additional pairs of arguments and argument descriptors that have unexpected argument descriptors, they will be removed from the URI. This mechanism allows future versions of the scheme to add additional command arguments without breaking backward compatibility with legacy implementations of this scheme.</span></span>
  
## <a name="17-implementation-restrictions-on-command-arguments"></a><span data-ttu-id="f9ff3-185">1.7 ОГРАНИЧЕНИЯ РЕАЛИЗАЦИИ АРГУМЕНТОВ КОМАНД</span><span class="sxs-lookup"><span data-stu-id="f9ff3-185">1.7 IMPLEMENTATION RESTRICTIONS ON COMMAND ARGUMENTS</span></span>

<span data-ttu-id="f9ff3-186">Следующие ограничения применяются к аргументам команд в текущей реализации Office 2013.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-186">The below restrictions are placed on command arguments in its current implementation in Office 2013.</span></span>
  
### <a name="length-limitations-on-uri-command-arguments"></a><span data-ttu-id="f9ff3-187">Ограничения длины аргументов команд URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-187">Length limitations on URI command arguments</span></span>

<span data-ttu-id="f9ff3-p114">Максимальная длина пути аргументов команд URI составляет 256 символов для всех приложений, кроме Excel, для которого ограничение  216 символов. Пути с большей длиной могут поддерживаться в различных приложениях, перед развертыванием подобных решений рекомендуется тщательно их протестировать.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p114">For URI command arguments, the maximum path length is 256 characters for all apps except Excel, where the limit is 216. Path lengths greater than these may be supported on an app-by-app basis and testing is recommended before deploying any solutions that rely on this.</span></span>
  
### <a name="allowed-characters-in-uri-command-arguments"></a><span data-ttu-id="f9ff3-190">Допустимые символы в аргументах команд URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-190">Allowed characters in URI command arguments</span></span>

<span data-ttu-id="f9ff3-p115">Допустимые URI должны соответствовать стандартам, предложенным в документе RFC 3987  интернационализированным идентификаторам ресурса (IRI). Символы, которые определены в RFC 3986 как зарезервированные, должны кодироваться с использованием символа процента. Имена файлов не должны содержать следующие символы: \ / : ? \< \> | " и \*.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p115">Allowed URIs must conform to the standards proposed in RFC 3987 - Internationalized Resource Identifiers (IRIs) . Characters identified as reserved in RFC 3986 should not be percent encoded. . Filenames must not contain any of the following characters: \ / : ? \< \> | " or \*.</span></span>  
  
## <a name="appendix-a---uri-scheme-registration-template-for-ms-word-scheme"></a><span data-ttu-id="f9ff3-196">ПРИЛОЖЕНИЕ А. ШАБЛОН РЕГИСТРАЦИИ СХЕМЫ URI ДЛЯ СХЕМЫ MS-WORD</span><span class="sxs-lookup"><span data-stu-id="f9ff3-196">APPENDIX A - URI SCHEME REGISTRATION TEMPLATE FOR MS-WORD SCHEME</span></span>
<span data-ttu-id="f9ff3-197"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="f9ff3-197"><a name="bk_addresources"> </a></span></span>

### <a name="a-3-uri-scheme-syntax"></a><span data-ttu-id="f9ff3-p116">А-3. Синтаксис схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p116">A-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="f9ff3-200">Схема Word = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="f9ff3-200">Word Scheme = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="f9ff3-201">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-201">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-202">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-202">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-203">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="f9ff3-203">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="f9ff3-204">document-uri = URI документа, который требуется открыть</span><span class="sxs-lookup"><span data-stu-id="f9ff3-204">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="f9ff3-205">template-uri = URI файла шаблона, на котором будет основан новый файл</span><span class="sxs-lookup"><span data-stu-id="f9ff3-205">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="f9ff3-206">save-location = URI папки, в которой будет создан документ</span><span class="sxs-lookup"><span data-stu-id="f9ff3-206">save-location = URI location of folder in which new document should be created</span></span>
    
### <a name="a-4-uri-scheme-semantics"></a><span data-ttu-id="f9ff3-p117">А-4. Семантика схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p117">A-4. URI Scheme Semantics</span></span>

<span data-ttu-id="f9ff3-p118">Схема ms-word определяет синтаксис URI для открытия или создания документа Word. В ней определены три команды, которые указывают, что необходимо сделать с указанным документом. Это команды: 1) open-for-edit-cmd (ofe), которая приводит к открытию документа по указанному URI в приложении для редактирования; 2) open-for-view-cmd (ofv), которая приводит к открытию документа по указанному URI в приложении в режиме только для чтения; 3) new-from-template-cmd (nft), которая приводит к созданию документа в приложении на основе шаблона по указанному в template-uri идентификатору URI и сохранению документа в расположении, указанном в необязательном аргументе save-location или, при его отсутствии, в библиотеке документов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p118">The ms-word scheme defines a URI syntax for opening or creating a word processing document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a word processing application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a word processing application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a word processing application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="a-5-applicationsprotocols-that-use-the-ms-word-uri-scheme"></a><span data-ttu-id="f9ff3-p119">А-5. Приложения и протоколы, использующие схему URI ms-word</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p119">A-5. Applications/Protocols that use the ms-word URI Scheme</span></span>

<span data-ttu-id="f9ff3-p120">Схема URI ms-word используется Microsoft Office 2013 для вызова Microsoft Word 2013 или Microsoft Word 2010 с пакетом обновлений 2 (SP2). Microsoft SharePoint 2013 использует URI ms-word как ссылки на документы Word, хранящиеся в библиотеках документов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p120">The ms-word URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Word 2013 or Microsoft Word 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-word URIs as links to word processing documents stored in SharePoint document libraries.</span></span>
  
### <a name="a-6-interoperability-considerations"></a><span data-ttu-id="f9ff3-p121">А-6. Вопросы взаимодействия</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p121">A-6. Interoperability Considerations</span></span>

<span data-ttu-id="f9ff3-p122">Обратите внимание, что вертикальная черта, используемая как разделитель в этой спецификации, не входит в число символов, определенных в разделе 2.2 документа RFC 3986 как зарезервированные для возможного использования в качестве разделителей. Это сделано специально, чтобы расширить число символов, поддерживаемых аргументами команд URI без их кодирования с использованием символа процента.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p122">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters.. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="f9ff3-220">В сегментах < *command-argument*  > зарезервированные RFC 3986 символы ":" и "/" входят в данные аргумента, а не представляют разделители, поэтому их можно добавлять без экранирования.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-220">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="a-7-security-considerations"></a><span data-ttu-id="f9ff3-p123">А-7. Вопросы безопасности</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p123">A-7. Security Considerations</span></span>

 <span data-ttu-id="f9ff3-p124">В системах с зарегистрированными обработчиками, которые распознают URI ms-word, переход по ссылке на URI ms-word приводит к запуску зарегистрированного текстового процессора и попытке открыть документ по указанному URI. Текстовые процессоры, регистрируемые для обработки URI ms-word, должны реализовать средства защиты от открытия документов из недоверенных удаленных систем, которые могут содержать вредоносный код.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p124">On systems that have registered handlers to recognize and act on ms-word URIs, clicking on a link to an ms-word URI will cause the registered word processing application to be launched, with instructions to the word processing application to attempt to open a document at the specified URI. Word processing applications registering to process ms-word URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span> 
  
### <a name="a-8-references"></a><span data-ttu-id="f9ff3-p125">А-8. Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p125">A-8. References</span></span>

<span data-ttu-id="f9ff3-227">RFC 3987  интернационализированные идентификаторы ресурса (IRI)</span><span class="sxs-lookup"><span data-stu-id="f9ff3-227">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-b---uri-scheme-registration-template-for-ms-powerpoint-scheme"></a><span data-ttu-id="f9ff3-228">ПРИЛОЖЕНИЕ Б. ШАБЛОН РЕГИСТРАЦИИ СХЕМЫ URI ДЛЯ СХЕМЫ MS-POWERPOINT</span><span class="sxs-lookup"><span data-stu-id="f9ff3-228">APPENDIX B - URI SCHEME REGISTRATION TEMPLATE FOR MS-POWERPOINT SCHEME</span></span>
<span data-ttu-id="f9ff3-229"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="f9ff3-229"><a name="bk_addresources"> </a></span></span>

### <a name="b-3-uri-scheme-syntax"></a><span data-ttu-id="f9ff3-p126">Б-3. Синтаксис схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p126">B-3. URI Scheme Syntax</span></span>

- <span data-ttu-id="f9ff3-232">Схема PowerPoint = "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="f9ff3-232">PowerPoint Scheme = "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
- <span data-ttu-id="f9ff3-233">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-233">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
- <span data-ttu-id="f9ff3-234">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-234">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
- <span data-ttu-id="f9ff3-235">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="f9ff3-235">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
- <span data-ttu-id="f9ff3-236">document-uri = URI документа, который требуется открыть</span><span class="sxs-lookup"><span data-stu-id="f9ff3-236">document-uri = URI location of document to open</span></span>
    
- <span data-ttu-id="f9ff3-237">template-uri = URI файла шаблона, на котором будет основан новый файл</span><span class="sxs-lookup"><span data-stu-id="f9ff3-237">template-uri = URI location of template file upon which new file will be based</span></span>
    
- <span data-ttu-id="f9ff3-238">save-location\* = URI папки, в которой будет создан документ</span><span class="sxs-lookup"><span data-stu-id="f9ff3-238">save-location\* = URI location of folder in which new document should be created</span></span>
    
- <span data-ttu-id="f9ff3-239">\*save-location  это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="f9ff3-239">\*save-location is an optional parameter</span></span>
    
### <a name="b-4-uri-scheme-semantics"></a><span data-ttu-id="f9ff3-p127">B-4. Семантика схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p127">B-4. URI Scheme Semantics</span></span>

<span data-ttu-id="f9ff3-p128">Схема ms-powerpoint определяет синтаксис URI для открытия или создания презентации. В ней определены три команды, которые указывают, что необходимо сделать с указанным документом. Это команды: 1) open-for-edit-cmd (ofe), которая приводит к открытию презентации по указанному URI в приложении для редактирования; 2) open-for-view-cmd (ofv), которая приводит к открытию презентации по указанному URI в приложении в режиме только для чтения; 3) new-from-template-cmd (nft), которая приводит к созданию презентации в приложении на основе шаблона по указанному в template-uri идентификатору URI и сохранению документа в расположении, указанном в необязательном аргументе save-location или, при его отсутствии, в библиотеке документов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p128">The ms-powerpoint scheme defines a URI syntax for opening or creating a presentation document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a presentation application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a presentation application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a presentation application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="b-5-applicationsprotocols-that-use-the-ms-powerpoint-uri-scheme"></a><span data-ttu-id="f9ff3-p129">Б-5. Приложения и протоколы, использующие схему URI ms-powerpoint</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p129">B-5. Applications/Protocols that use the ms-powerpoint URI Scheme</span></span>

<span data-ttu-id="f9ff3-p130">Схема URI ms-powerpoint используется Microsoft Office 2013 для вызова Microsoft PowerPoint 2013 или Microsoft PowerPoint 2010 с пакетом обновлений 2 (SP2). Microsoft SharePoint 2013 использует URI ms-powerpoint как ссылки на презентации, хранящиеся в библиотеках документов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p130">The ms-powerpoint URI Scheme is used by Microsoft Office 2013 to invoke Microsoft PowerPoint 2013 or Microsoft PowerPoint 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-powerpoint URIs as links to presentation documents stored in SharePoint document libraries.</span></span>
  
### <a name="b-6-interoperability-considerations"></a><span data-ttu-id="f9ff3-p131">Б-6. Вопросы взаимодействия</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p131">B-6. Interoperability Considerations</span></span>

<span data-ttu-id="f9ff3-p132">Обратите внимание, что вертикальная черта, используемая как разделитель в этой спецификации, не входит в число символов, определенных в разделе 2.2 документа RFC 3986 как зарезервированные для возможного использования в качестве разделителей. Это сделано специально, чтобы расширить число символов, поддерживаемых аргументами команд URI без их кодирования с использованием символа процента.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p132">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="f9ff3-253">В сегментах < *command-argument*  > зарезервированные RFC 3986 символы ":" и "/" входят в данные аргумента, а не представляют разделители, поэтому их можно добавлять без экранирования.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-253">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="b-7-security-considerations"></a><span data-ttu-id="f9ff3-p133">Б-7. Вопросы безопасности</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p133">B-7. Security Considerations</span></span>

<span data-ttu-id="f9ff3-p134">В системах с зарегистрированными обработчиками, которые распознают URI ms-powerpoint, переход по ссылке на URI ms-powerpoint приводит к запуску зарегистрированного приложения для работы с презентациями и попытке открыть документ по указанному URI. Приложения для работы с презентациями, регистрируемые для обработки URI ms-powerpoint, должны реализовать средства защиты от открытия документов из недоверенных удаленных систем, которые могут содержать вредоносный код.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p134">On systems that have registered handlers to recognize and act on ms-powerpoint URIs, clicking on a link to an ms-powerpoint URI will cause the registered presentation application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-powerpoint URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="b-8-references"></a><span data-ttu-id="f9ff3-p135">Б-8. Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p135">B-8. References</span></span>

<span data-ttu-id="f9ff3-260">RFC 3987  интернационализированные идентификаторы ресурса (IRI)</span><span class="sxs-lookup"><span data-stu-id="f9ff3-260">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-c---uri-scheme-registration-template-for-ms-excel-scheme"></a><span data-ttu-id="f9ff3-261">ПРИЛОЖЕНИЕ В. ШАБЛОН РЕГИСТРАЦИИ СХЕМЫ URI ДЛЯ СХЕМЫ MS-EXCEL</span><span class="sxs-lookup"><span data-stu-id="f9ff3-261">APPENDIX C - URI SCHEME REGISTRATION TEMPLATE FOR MS-EXCEL SCHEME</span></span>
<span data-ttu-id="f9ff3-262"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="f9ff3-262"><a name="bk_addresources"> </a></span></span>

### <a name="c-3-uri-scheme-syntax"></a><span data-ttu-id="f9ff3-p136">В-3. Синтаксис схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p136">C-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="f9ff3-265">Схема Excel = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="f9ff3-265">Excel Scheme = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="f9ff3-266">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-266">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-267">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-267">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-268">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="f9ff3-268">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="f9ff3-269">document-uri = URI документа, который требуется открыть</span><span class="sxs-lookup"><span data-stu-id="f9ff3-269">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="f9ff3-270">template-uri = URI файла шаблона, на котором будет основан новый файл</span><span class="sxs-lookup"><span data-stu-id="f9ff3-270">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="f9ff3-271">save-location\* = URI папки, в которой будет создан документ</span><span class="sxs-lookup"><span data-stu-id="f9ff3-271">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="f9ff3-272">\*save-location  это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="f9ff3-272">\*save-location is an optional parameter</span></span>
    
### <a name="c-4-uri-scheme-semantics"></a><span data-ttu-id="f9ff3-p137">В-4. Семантика схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p137">C-4. URI Scheme Semantics</span></span>

<span data-ttu-id="f9ff3-p138">Схема ms-excel определяет синтаксис URI для открытия или создания электронной таблицы. В ней определены три команды, которые указывают, что необходимо сделать с указанным документом. Это команды: 1) open-for-edit-cmd (ofe), которая приводит к открытию электронной таблицы по указанному URI в приложении для редактирования; 2) open-for-view-cmd (ofv), которая приводит к открытию электронной таблицы по указанному URI в приложении в режиме только для чтения; 3) new-from-template-cmd (nft), которая приводит к созданию электронной таблицы в приложении на основе шаблона по указанному в template-uri идентификатору URI и сохранению документа в расположении, указанном в необязательном аргументе save-location или, при его отсутствии, в библиотеке документов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p138">The ms-excel scheme defines a URI syntax for opening or creating a spreadsheet document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a spreadsheet application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a spreadsheet application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a spreadsheet application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="c-5-applicationsprotocols-that-use-the-ms-excel-uri-scheme"></a><span data-ttu-id="f9ff3-p139">В-5. Приложения и протоколы, использующие схему URI ms-excel</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p139">C-5. Applications/Protocols that use the ms-excel URI Scheme</span></span>

<span data-ttu-id="f9ff3-p140">Схема URI ms-excel используется Microsoft Office 2013 для вызова Microsoft Excel 2013 или Microsoft Excel 2010 с пакетом обновлений 2 (SP2). Microsoft SharePoint 2013 использует URI ms-excel как ссылки на электронные таблицы, хранящиеся в библиотеках документов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p140">The ms-excel URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Excel 2013 or Microsoft Excel 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-excel URIs as links to spreadsheet documents stored in SharePoint document libraries.</span></span>
  
### <a name="c-6-interoperability-considerations"></a><span data-ttu-id="f9ff3-p141">В-6. Вопросы взаимодействия</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p141">C-6. Interoperability Considerations</span></span>

<span data-ttu-id="f9ff3-p142">Обратите внимание, что вертикальная черта, используемая как разделитель в этой спецификации, не входит в число символов, определенных в разделе 2.2 документа RFC 3986 как зарезервированные для возможного использования в качестве разделителей. Это сделано специально, чтобы расширить число символов, поддерживаемых аргументами команд URI без их кодирования с использованием символа процента.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p142">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="f9ff3-286">В сегментах < *command-argument*  > зарезервированные RFC 3986 символы ":" и "/" входят в данные аргумента, а не представляют разделители, поэтому их можно добавлять без экранирования.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-286">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="c-7-security-considerations"></a><span data-ttu-id="f9ff3-p143">В-7. Вопросы безопасности</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p143">C-7. Security Considerations</span></span>

<span data-ttu-id="f9ff3-p144">В системах с зарегистрированными обработчиками, которые распознают URI ms-excel, переход по ссылке на URI ms-excel приводит к запуску зарегистрированного приложения для работы с электронными таблицами и попытке открыть документ по указанному URI. Приложения для работы с электронными таблицами, регистрируемые для обработки URI ms-excel, должны реализовать средства защиты от открытия документов из недоверенных удаленных систем, которые могут содержать вредоносный код.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p144">On systems that have registered handlers to recognize and act on ms-excel URIs, clicking on a link to an ms-excel URI will cause the registered spreadsheet application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-excel URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="c-8-references"></a><span data-ttu-id="f9ff3-p145">В-8. Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p145">C-8. References</span></span>

<span data-ttu-id="f9ff3-293">RFC 3987  интернационализированные идентификаторы ресурса (IRI)</span><span class="sxs-lookup"><span data-stu-id="f9ff3-293">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-d---uri-scheme-registration-template-for-ms-visio-scheme"></a><span data-ttu-id="f9ff3-294">ПРИЛОЖЕНИЕ Г. ШАБЛОН РЕГИСТРАЦИИ СХЕМЫ URI ДЛЯ СХЕМЫ MS-VISIO</span><span class="sxs-lookup"><span data-stu-id="f9ff3-294">APPENDIX D - URI SCHEME REGISTRATION TEMPLATE FOR MS-VISIO SCHEME</span></span>
<span data-ttu-id="f9ff3-295"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="f9ff3-295"><a name="bk_addresources"> </a></span></span>

### <a name="d-3-uri-scheme-syntax"></a><span data-ttu-id="f9ff3-p146">Г-3. Синтаксис схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p146">D-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="f9ff3-298">Схема Visio = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="f9ff3-298">Visio Scheme = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="f9ff3-299">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-299">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-300">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-300">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-301">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="f9ff3-301">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="f9ff3-302">document-uri = URI документа, который требуется открыть</span><span class="sxs-lookup"><span data-stu-id="f9ff3-302">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="f9ff3-303">template-uri = URI файла шаблона, на котором будет основан новый файл</span><span class="sxs-lookup"><span data-stu-id="f9ff3-303">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="f9ff3-304">save-location\* = URI папки, в которой будет создан документ</span><span class="sxs-lookup"><span data-stu-id="f9ff3-304">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="f9ff3-305">\*save-location  это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="f9ff3-305">\*save-location is an optional parameter</span></span>
    
### <a name="d-4-uri-scheme-semantics"></a><span data-ttu-id="f9ff3-p147">Г-4. Семантика схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p147">D-4. URI Scheme Semantics</span></span>

<span data-ttu-id="f9ff3-p148">Схема ms-visio определяет синтаксис URI для открытия или создания документа Microsoft Visio. В ней определены три команды, которые указывают, что необходимо сделать с указанным документом. Это команды: 1) open-for-edit-cmd (ofe), которая приводит к открытию документа по указанному URI в приложении Visio для редактирования; 2) open-for-view-cmd (ofv), которая приводит к открытию документа по указанному URI в приложении Visio в режиме только для чтения; 3) new-from-template-cmd (nft), которая приводит к созданию документа в приложении Visio на основе шаблона по указанному в template-uri идентификатору URI и сохранению документа в расположении, указанном в необязательном аргументе save-location или, при его отсутствии, в библиотеке документов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p148">The ms-visio scheme defines a URI syntax for opening or creating a Microsoft Visio document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Visio to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Visio to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Visio to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="d-5-applicationsprotocols-that-use-the-ms-visio-uri-scheme"></a><span data-ttu-id="f9ff3-p149">Г-5. Приложения и протоколы, использующие схему URI ms-visio</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p149">D-5. Applications/Protocols that use the ms-visio URI Scheme</span></span>

<span data-ttu-id="f9ff3-p150">Схема URI ms-visio используется Microsoft Office 2013 для вызова Microsoft Visio 2013 или Microsoft Visio 2010 с пакетом обновлений 2 (SP2). Microsoft SharePoint 2013 использует URI ms-visio как ссылки на документы Visio, хранящиеся в библиотеках документов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p150">The ms-visio URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Visio 2013 or Microsoft Visio 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-visio URIs as links to Visio documents stored in SharePoint document libraries.</span></span>
  
### <a name="d-6-interoperability-considerations"></a><span data-ttu-id="f9ff3-p151">Г-6. Вопросы взаимодействия</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p151">D-6. Interoperability Considerations</span></span>

<span data-ttu-id="f9ff3-p152">Обратите внимание, что вертикальная черта, используемая как разделитель в этой спецификации, не входит в число символов, определенных в разделе 2.2 документа RFC 3986 как зарезервированные для возможного использования в качестве разделителей. Это сделано специально, чтобы расширить число символов, поддерживаемых аргументами команд URI без их кодирования с использованием символа процента.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p152">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="f9ff3-319">В сегментах < *command-argument*  > зарезервированные RFC 3986 символы ":" и "/" входят в данные аргумента, а не представляют разделители, поэтому их можно добавлять без экранирования.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-319">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="d-7-security-considerations"></a><span data-ttu-id="f9ff3-p153">Г-7. Вопросы безопасности</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p153">D-7. Security Considerations</span></span>

<span data-ttu-id="f9ff3-p154">В системах с зарегистрированными обработчиками, которые распознают URI ms-visio, переход по ссылке на URI ms-powerpoint приводит к запуску зарегистрированного приложения и попытке открыть документ по указанному URI. Приложения, регистрируемые для обработки URI ms-visio, должны реализовать средства защиты от открытия документов из недоверенных удаленных систем, которые могут содержать вредоносный код.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p154">On systems that have registered handlers to recognize and act on ms-visio URIs, clicking on a link to an ms-visio URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-visio URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="d-8-references"></a><span data-ttu-id="f9ff3-p155">Г-8. Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p155">D-8. References</span></span>

<span data-ttu-id="f9ff3-326">RFC 3987  интернационализированные идентификаторы ресурса (IRI)</span><span class="sxs-lookup"><span data-stu-id="f9ff3-326">RFC 3987 - International Resource Identifiers (IRIs)</span></span>
  
## <a name="appendix-e---uri-scheme-registration-template-for-ms-access-scheme"></a><span data-ttu-id="f9ff3-327">ПРИЛОЖЕНИЕ Д. ШАБЛОН РЕГИСТРАЦИИ СХЕМЫ URI ДЛЯ СХЕМЫ MS-ACCESS</span><span class="sxs-lookup"><span data-stu-id="f9ff3-327">APPENDIX E - URI SCHEME REGISTRATION TEMPLATE FOR MS-ACCESS SCHEME</span></span>
<span data-ttu-id="f9ff3-328"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="f9ff3-328"><a name="bk_addresources"> </a></span></span>

### <a name="e-3-uri-scheme-syntax"></a><span data-ttu-id="f9ff3-p156">Д-3. Синтаксис схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p156">E-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="f9ff3-331">Схема Access = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="f9ff3-331">Access Scheme = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="f9ff3-332">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-332">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-333">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-333">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-334">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="f9ff3-334">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="f9ff3-335">document-uri = URI документа, который требуется открыть</span><span class="sxs-lookup"><span data-stu-id="f9ff3-335">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="f9ff3-336">template-uri = URI файла шаблона, на котором будет основан новый файл</span><span class="sxs-lookup"><span data-stu-id="f9ff3-336">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="f9ff3-337">save-location\* = URI папки, в которой будет создан документ</span><span class="sxs-lookup"><span data-stu-id="f9ff3-337">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="f9ff3-338">\*save-location  это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="f9ff3-338">\*save-location is an optional parameter</span></span>
    
### <a name="e-4-uri-scheme-semantics"></a><span data-ttu-id="f9ff3-p157">Д-4. Семантика схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p157">E-4. URI Scheme Semantics</span></span>

<span data-ttu-id="f9ff3-p158">Схема ms-access определяет синтаксис URI для открытия или создания базы данных. В ней определены три команды, которые указывают, что необходимо сделать с указанным файлом базы данных. Это команды: 1) open-for-edit-cmd (ofe), которая приводит к открытию базы данных по указанному URI в приложении для редактирования; 2) open-for-view-cmd (ofv), которая приводит к открытию базы данных по указанному URI в приложении в режиме только для чтения; 3) new-from-template-cmd (nft), которая приводит к созданию базы данных в приложении на основе шаблона по указанному в template-uri идентификатору URI и сохранению базы данных в расположении, указанном в необязательном аргументе save-location или, при его отсутствии, в библиотеке документов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p158">The ms-access scheme defines a URI syntax for opening or creating a database. The scheme defines three commands that serve as instructions regarding what should be done with the referenced database file. The commands are 1) open-for-edit-cmd (ofe), which instructs the database application to open the database at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs the database application to open the database at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs the database application to create a new database based on the template located at the specified template-uri URI and save the new database either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="e-5-applicationsprotocols-that-use-the-ms-access-uri-scheme"></a><span data-ttu-id="f9ff3-p159">Д-5. Приложения и протоколы, использующие схему URI ms-access</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p159">E-5. Applications/Protocols that use the ms-access URI Scheme</span></span>

<span data-ttu-id="f9ff3-p160">Схема URI ms-access используется Microsoft Office 2013 для вызова Microsoft Access 2013 или Microsoft Access 2010 с пакетом обновлений 2 (SP2) из веб-страниц. Microsoft SharePoint 2013 использует URI ms-access как ссылки на базы данных Access, хранящиеся в библиотеках документов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p160">The ms-access URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Access 2013 or Microsoft Access 2010 with Service Pack 2 from web pages. Microsoft SharePoint 2013 uses ms-access URIs as links to Access databases stored in SharePoint document libraries.</span></span>
  
### <a name="e-6-interoperability-considerations"></a><span data-ttu-id="f9ff3-p161">Д-6. Вопросы взаимодействия</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p161">E-6. Interoperability Considerations</span></span>

<span data-ttu-id="f9ff3-p162">Обратите внимание, что вертикальная черта, используемая как разделитель в этой спецификации, не входит в число символов, определенных в разделе 2.2 документа RFC 3986 как зарезервированные для возможного использования в качестве разделителей. Это сделано специально, чтобы расширить число символов, поддерживаемых аргументами команд URI без их кодирования с использованием символа процента. В сегментах \<command-argument\> зарезервированные RFC 3986 символы ":" и "/" входят в данные аргумента, а не представляют разделители, поэтому их можно добавлять без экранирования.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p162">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. Within \<command-argument\> segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span>
  
### <a name="e-7-security-considerations"></a><span data-ttu-id="f9ff3-p163">Д-7. Вопросы безопасности</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p163">E-7. Security Considerations</span></span>

<span data-ttu-id="f9ff3-p164">В системах с зарегистрированными обработчиками, которые распознают URI ms-access, переход по ссылке на URI ms-access приводит к запуску зарегистрированного приложения и попытке открыть базу данных по указанному URI. Приложения, регистрируемые для обработки URI ms-access, должны реализовать средства защиты от открытия баз данных из недоверенных удаленных систем, которые могут содержать вредоносный код.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p164">On systems that have registered handlers to recognize and act on ms-access URIs, clicking on a link to an ms-access URI will cause the registered application to be launched, with instructions to the application to attempt to open a database at the specified URI. Applications registering to process ms-access URIs should implement protections to guard against opening databases from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="e-8-references"></a><span data-ttu-id="f9ff3-p165">Д-8. Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p165">E-8. References</span></span>

<span data-ttu-id="f9ff3-359">RFC 3987  интернационализированные идентификаторы ресурса (IRI)</span><span class="sxs-lookup"><span data-stu-id="f9ff3-359">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-f---uri-scheme-registration-template-for-ms-project-scheme"></a><span data-ttu-id="f9ff3-360">ПРИЛОЖЕНИЕ Е. ШАБЛОН РЕГИСТРАЦИИ СХЕМЫ URI ДЛЯ СХЕМЫ MS-PROJECT</span><span class="sxs-lookup"><span data-stu-id="f9ff3-360">APPENDIX F - URI SCHEME REGISTRATION TEMPLATE FOR MS-PROJECT SCHEME</span></span>
<span data-ttu-id="f9ff3-361"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="f9ff3-361"><a name="bk_addresources"> </a></span></span>

### <a name="f-3-uri-scheme-syntax"></a><span data-ttu-id="f9ff3-p166">Е-3. Синтаксис схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p166">F-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="f9ff3-364">Схема Project = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="f9ff3-364">Project Scheme = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="f9ff3-365">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-365">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-366">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-366">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-367">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="f9ff3-367">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="f9ff3-368">document-uri = URI документа, который требуется открыть</span><span class="sxs-lookup"><span data-stu-id="f9ff3-368">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="f9ff3-369">template-uri = URI файла шаблона, на котором будет основан новый файл</span><span class="sxs-lookup"><span data-stu-id="f9ff3-369">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="f9ff3-370">save-location\* = URI папки, в которой будет создан документ</span><span class="sxs-lookup"><span data-stu-id="f9ff3-370">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="f9ff3-371">\*save-location  это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="f9ff3-371">\*save-location is an optional parameter</span></span>
    
### <a name="f-4-uri-scheme-semantics"></a><span data-ttu-id="f9ff3-p167">Е-4. Семантика схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p167">F-4. URI Scheme Semantics</span></span>

<span data-ttu-id="f9ff3-p168">Схема ms-project определяет синтаксис URI для открытия или создания документа Microsoft Project. В ней определены три команды, которые указывают, что необходимо сделать с указанным документом. Это команды: 1) open-for-edit-cmd (ofe), которая приводит к открытию документа по указанному URI в приложении Project для редактирования; 2) open-for-view-cmd (ofv), которая приводит к открытию документа по указанному URI в приложении Project в режиме только для чтения; 3) new-from-template-cmd (nft), которая приводит к созданию документа в приложении Project на основе шаблона по указанному в template-uri идентификатору URI и сохранению документа в расположении, указанном в необязательном аргументе save-location или, при его отсутствии, в библиотеке документов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p168">The ms-project scheme defines a URI syntax for opening or creating a Microsoft Project document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Project to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Project to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Project to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="f-5-applicationsprotocols-that-use-the-ms-project-uri-scheme"></a><span data-ttu-id="f9ff3-p169">Е-5. Приложения и протоколы, использующие схему URI ms-project</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p169">F-5. Applications/Protocols that use the ms-project URI Scheme</span></span>

<span data-ttu-id="f9ff3-p170">Microsoft Office 2013 использует схему URI ms-project для вызова Microsoft Project 2013 из веб-страниц. Microsoft SharePoint 2013 использует URI ms-project как ссылки на документы Project, хранимые в библиотеках документов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p170">The ms-project URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Project 2013 from web pages. Microsoft SharePoint 2013 uses ms-project URIs as links to Project documents stored in SharePoint document libraries.</span></span>
  
### <a name="f-6-interoperability-considerations"></a><span data-ttu-id="f9ff3-p171">Е-6. Вопросы взаимодействия</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p171">F-6. Interoperability Considerations</span></span>

<span data-ttu-id="f9ff3-p172">Обратите внимание, что вертикальная черта, используемая как разделитель в этой спецификации, не входит в число символов, определенных в разделе 2.2 документа RFC 3986 как зарезервированные для возможного использования в качестве разделителей. Это сделано специально, чтобы расширить число символов, поддерживаемых аргументами команд URI без их кодирования с использованием символа процента.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p172">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="f9ff3-385">В сегментах < *command-argument*  > зарезервированные RFC 3986 символы ":" и "/" входят в данные аргумента, а не представляют разделители, поэтому их можно добавлять без экранирования.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-385">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="f-7-security-considerations"></a><span data-ttu-id="f9ff3-p173">Е-7. Вопросы безопасности</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p173">F-7. Security Considerations</span></span>

<span data-ttu-id="f9ff3-p174">В системах с зарегистрированными обработчиками, которые распознают URI ms-project, переход по ссылке на URI ms-project приводит к запуску зарегистрированного приложения и попытке открыть документ по указанному URI. Приложения, регистрируемые для обработки URI ms-project, должны реализовать средства защиты от открытия документов из недоверенных удаленных систем, которые могут содержать вредоносный код.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p174">On systems that have registered handlers to recognize and act on ms-project URIs, clicking on a link to an ms-project URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-project URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="f-8-references"></a><span data-ttu-id="f9ff3-p175">Е-8. Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p175">F-8. References</span></span>

<span data-ttu-id="f9ff3-392">RFC 3987  интернационализированные идентификаторы ресурса (IRI)</span><span class="sxs-lookup"><span data-stu-id="f9ff3-392">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-g---uri-scheme-registration-template-for-ms-publisher-scheme"></a><span data-ttu-id="f9ff3-393">ПРИЛОЖЕНИЕ Ж. ШАБЛОН РЕГИСТРАЦИИ СХЕМЫ URI ДЛЯ СХЕМЫ MS-PUBLISHER</span><span class="sxs-lookup"><span data-stu-id="f9ff3-393">APPENDIX G - URI SCHEME REGISTRATION TEMPLATE FOR MS-PUBLISHER SCHEME</span></span>
<span data-ttu-id="f9ff3-394"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="f9ff3-394"><a name="bk_addresources"> </a></span></span>

### <a name="g-3-uri-scheme"></a><span data-ttu-id="f9ff3-p176">Ж-3. Синтаксис схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p176">G-3. URI Scheme</span></span>

> <span data-ttu-id="f9ff3-397">Схема Publisher = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="f9ff3-397">Syntax Publisher Scheme = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="f9ff3-398">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-398">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-399">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-399">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-400">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="f9ff3-400">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="f9ff3-401">document-uri = URI документа, который требуется открыть</span><span class="sxs-lookup"><span data-stu-id="f9ff3-401">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="f9ff3-402">template-uri = URI файла шаблона, на котором будет основан новый файл</span><span class="sxs-lookup"><span data-stu-id="f9ff3-402">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="f9ff3-403">save-location\* = URI папки, в которой будет создан документ</span><span class="sxs-lookup"><span data-stu-id="f9ff3-403">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="f9ff3-404">\*save-location  это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="f9ff3-404">\*save-location is an optional parameter</span></span>
    
### <a name="g-4-uri-scheme-semantics"></a><span data-ttu-id="f9ff3-p177">Ж-4. Семантика схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p177">G-4. URI Scheme Semantics</span></span>

<span data-ttu-id="f9ff3-p178">Схема ms-publisher определяет синтаксис URI для открытия или создания документа Microsoft Publisher. В ней определены три команды, которые указывают, что необходимо сделать с указанным документом. Это команды: 1) open-for-edit-cmd (ofe), которая приводит к открытию документа по указанному URI в приложении Publisher для редактирования; 2) open-for-view-cmd (ofv), которая приводит к открытию документа по указанному URI в приложении Publisher в режиме только для чтения; 3) new-from-template-cmd (nft), которая приводит к созданию документа в приложении Publisher на основе шаблона по указанному в template-uri идентификатору URI и сохранению документа в расположении, указанном в необязательном аргументе save-location или, при его отсутствии, в библиотеке документов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p178">The ms-publisher scheme defines a URI syntax for opening or creating a Microsoft Publisher document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Publisher to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Publisher to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Publisher to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="g-5-applicationsprotocols-that-use-the-ms-publisher-uri-scheme"></a><span data-ttu-id="f9ff3-p179">Ж-5. Приложения и протоколы, использующие схему URI ms-publisher</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p179">G-5. Applications/Protocols that use the ms-publisher URI Scheme</span></span>

<span data-ttu-id="f9ff3-p180">Схема URI ms-publisher используется Microsoft Office 2013 для вызова Microsoft Publisher 2013 или Microsoft Publisher 2010 с пакетом обновлений 2 (SP2) из веб-страниц. Microsoft SharePoint 2013 использует URI ms-publisher как ссылки на документы Publisher, хранящиеся в библиотеках документов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p180">The ms-publisher URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Publisher 2013 or Microsoft Publisher 2010 with Service Pack 2 from web pages. Microsoft SharePoint 2013 uses ms-publisher URIs as links to Publisher documents stored in SharePoint document libraries.</span></span>
  
### <a name="g-6-interoperability-considerations"></a><span data-ttu-id="f9ff3-p181">Ж-6. Вопросы взаимодействия</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p181">G-6. Interoperability Considerations</span></span>

<span data-ttu-id="f9ff3-p182">Обратите внимание, что вертикальная черта, используемая как разделитель в этой спецификации, не входит в число символов, определенных в разделе 2.2 документа RFC 3986 как зарезервированные для возможного использования в качестве разделителей. Это сделано специально, чтобы расширить число символов, поддерживаемых аргументами команд URI без их кодирования с использованием символа процента. В сегментах \<command-argument\> зарезервированные RFC 3986 символы ":" и "/" входят в данные аргумента, а не представляют разделители, поэтому их можно добавлять без экранирования.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p182">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. Within \<command-argument\> segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span>
  
### <a name="g-7-security-considerations"></a><span data-ttu-id="f9ff3-p183">Ж-7. Вопросы безопасности</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p183">G-7. Security Considerations</span></span>

<span data-ttu-id="f9ff3-p184">В системах с зарегистрированными обработчиками, которые распознают URI ms-publisher, переход по ссылке на URI ms-publisher приводит к запуску зарегистрированного приложения и попытке открыть документ по указанному URI. Приложения, регистрируемые для обработки URI ms-publisher, должны реализовать средства защиты от открытия документов из недоверенных удаленных систем, которые могут содержать вредоносный код.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p184">On systems that have registered handlers to recognize and act on ms-publisher URIs, clicking on a link to an ms-publisher URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-publisher URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="g-9-references"></a><span data-ttu-id="f9ff3-p185">Ж-9. Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p185">G-9. References</span></span>

<span data-ttu-id="f9ff3-425">RFC 3987  интернационализированные идентификаторы ресурса (IRI)</span><span class="sxs-lookup"><span data-stu-id="f9ff3-425">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-h---uri-scheme-registration-template-for-ms-spd-scheme"></a><span data-ttu-id="f9ff3-426">ПРИЛОЖЕНИЕ З. ШАБЛОН РЕГИСТРАЦИИ СХЕМЫ URI ДЛЯ СХЕМЫ MS-SPD</span><span class="sxs-lookup"><span data-stu-id="f9ff3-426">APPENDIX H - URI SCHEME REGISTRATION TEMPLATE FOR MS-SPD SCHEME</span></span>
<span data-ttu-id="f9ff3-427"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="f9ff3-427"><a name="bk_addresources"> </a></span></span>

### <a name="h-3-uri-scheme-syntax"></a><span data-ttu-id="f9ff3-p186">З-3. Синтаксис схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p186">H-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="f9ff3-430">Схема SharePoint Designer = "ms-spd:" open-for-edit-cmd</span><span class="sxs-lookup"><span data-stu-id="f9ff3-430">SharePoint Designer Scheme = "ms-spd:" open-for-edit-cmd</span></span>
    
> <span data-ttu-id="f9ff3-431">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-431">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-432">document-uri = URI документа, который требуется открыть</span><span class="sxs-lookup"><span data-stu-id="f9ff3-432">document-uri = URI location of document to open</span></span>
    
### <a name="h-4-uri-scheme-semantics"></a><span data-ttu-id="f9ff3-p187">З-4. Семантика схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p187">H-4. URI Scheme Semantics</span></span>

<span data-ttu-id="f9ff3-p188">Схема ms-spd определяет синтаксис URI для открытия документа Microsoft SharePoint Designer. В ней определены две команды, которые указывают, что необходимо сделать с указанным документом. Это команды: 1) open-for-edit-cmd (ofe), которая приводит к открытию в SharePoint Designer документа по указанному URI для редактирования; 2) open-for-view-cmd (ofv), которая приводит к открытию в SharePoint Designer документа по указанному URI в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p188">The ms-spd scheme defines a URI syntax for opening a Microsoft SharePoint Designer document. The scheme defines two commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs SharePoint Designer to open the document at the specified URI for editing; and 2) open-for-view-cmd (ofv), which instructs SharePoint Designer to open the document at the specified URI in a read-only mode.</span></span>
  
### <a name="h-5-applicationsprotocols-that-use-the-ms-spd-uri-scheme"></a><span data-ttu-id="f9ff3-p189">З-5. Приложения и протоколы, использующие схему URI ms-spd</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p189">H-5. Applications/Protocols that use the ms-spd URI Scheme</span></span>

<span data-ttu-id="f9ff3-p190">Microsoft Office 2013 использует схему URI ms-spd для вызова Microsoft SharePoint Designer 2013 из веб-страниц. Microsoft SharePoint 2013 использует URI ms-spd как ссылки на документы SharePoint Designer, хранимые в библиотеках документов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p190">The ms-spd URI Scheme is used by Microsoft Office 2013 to invoke Microsoft SharePoint Designer 2013 from web pages. Microsoft SharePoint 2013 uses ms-spd URIs as links to SharePoint Designer documents stored in SharePoint document libraries.</span></span>
  
### <a name="h-6-interoperability-considerations"></a><span data-ttu-id="f9ff3-p191">З-6. Вопросы взаимодействия</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p191">H-6. Interoperability Considerations</span></span>

<span data-ttu-id="f9ff3-p192">Обратите внимание, что вертикальная черта, используемая как разделитель в этой спецификации, не входит в число символов, определенных в разделе 2.2 документа RFC 3986 как зарезервированные для возможного использования в качестве разделителей. Это сделано специально, чтобы расширить число символов, поддерживаемых аргументами команд URI без их кодирования с использованием символа процента.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p192">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="f9ff3-446">В сегментах < *command-argument*  > зарезервированные RFC 3986 символы ":" и "/" входят в данные аргумента, а не представляют разделители, поэтому их можно добавлять без экранирования.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-446">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="h-7-security-considerations"></a><span data-ttu-id="f9ff3-p193">З-7. Вопросы безопасности</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p193">H-7. Security Considerations</span></span>

<span data-ttu-id="f9ff3-p194">В системах с зарегистрированными обработчиками, которые распознают URI ms-spd, переход по ссылке на URI ms-spd приводит к запуску зарегистрированного приложения и попытке открыть документ по указанному URI. Приложения, регистрируемые для обработки URI ms-spd, должны реализовать средства защиты от открытия документов из недоверенных удаленных систем, которые могут содержать вредоносный код.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p194">On systems that have registered handlers to recognize and act on ms-spd URIs, clicking on a link to an ms-spd URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-spd URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="h-8-references"></a><span data-ttu-id="f9ff3-p195">З-8. Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p195">H-8. References</span></span>

<span data-ttu-id="f9ff3-453">RFC 3987  интернационализированные идентификаторы ресурса (IRI)</span><span class="sxs-lookup"><span data-stu-id="f9ff3-453">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-i---uri-scheme-registration-template-for-ms-infopath-scheme"></a><span data-ttu-id="f9ff3-454">ПРИЛОЖЕНИЕ И. ШАБЛОН РЕГИСТРАЦИИ СХЕМЫ URI ДЛЯ СХЕМЫ MS-INFOPATH</span><span class="sxs-lookup"><span data-stu-id="f9ff3-454">APPENDIX I - URI SCHEME REGISTRATION TEMPLATE FOR MS-INFOPATH SCHEME</span></span>
<span data-ttu-id="f9ff3-455"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="f9ff3-455"><a name="bk_addresources"> </a></span></span>

###   <a name="i-3-uri-scheme-syntax"></a><span data-ttu-id="f9ff3-p196">И-3. Синтаксис схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p196">I-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="f9ff3-458">Схема Infopath = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd</span><span class="sxs-lookup"><span data-stu-id="f9ff3-458">Infopath Scheme = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd</span></span>
    
> <span data-ttu-id="f9ff3-459">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-459">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-460">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="f9ff3-460">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="f9ff3-461">document-uri = URI документа, который требуется открыть</span><span class="sxs-lookup"><span data-stu-id="f9ff3-461">document-uri = URI location of document to open</span></span>
    
### <a name="i-4-uri-scheme-semantics"></a><span data-ttu-id="f9ff3-p197">И-4. Семантика схемы URI</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p197">I-4. URI Scheme Semantics</span></span>

<span data-ttu-id="f9ff3-p198">Схема ms-infopath определяет синтаксис URI для открытия или создания документа Microsoft Infopath. В ней определены две команды, которые указывают, что необходимо сделать с указанным документом. Это команды: 1) open-for-edit-cmd (ofe), которая приводит к открытию в Visio документа по указанному URI для редактирования; 2) open-for-view-cmd (ofv), которая приводит к открытию в Visio документа по указанному URI в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p198">The ms-infopath scheme defines a URI syntax for opening or creating a Microsoft Infopath document. The scheme defines two commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Visio to open the document at the specified URI for editing; and 2) open-for-view-cmd (ofv), which instructs Visio to open the document at the specified URI in a read-only mode.</span></span>
  
### <a name="i-5-applicationsprotocols-that-use-the-ms-infopath-uri-scheme"></a><span data-ttu-id="f9ff3-p199">И-5. Приложения и протоколы, использующие схему URI ms-infopath</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p199">I-5. Applications/Protocols that use the ms-infopath URI Scheme</span></span>

<span data-ttu-id="f9ff3-p200">Microsoft Office 2013 использует схему URI ms-infopath для вызова Microsoft Infopath 2013 из веб-страниц. Microsoft SharePoint 2013 использует URI ms-infopath как ссылки на документы Infopath, хранимые в библиотеках документов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p200">The ms-infopath URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Infopath 2013 from web pages. Microsoft SharePoint 2013 uses ms-infopath URIs as links to Infopath documents stored in SharePoint document libraries.</span></span>
  
### <a name="i-6-interoperability-considerations"></a><span data-ttu-id="f9ff3-p201">И-6. Вопросы взаимодействия</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p201">I-6. Interoperability Considerations</span></span>

<span data-ttu-id="f9ff3-p202">Обратите внимание, что вертикальная черта, используемая как разделитель в этой спецификации, не входит в число символов, определенных в разделе 2.2 документа RFC 3986 как зарезервированные для возможного использования в качестве разделителей. Это сделано специально, чтобы расширить число символов, поддерживаемых аргументами команд URI без их кодирования с использованием символа процента.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p202">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="f9ff3-475">В сегментах < *command-argument*  > зарезервированные RFC 3986 символы ":" и "/" входят в данные аргумента, а не представляют разделители, поэтому их можно добавлять без экранирования.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-475">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="i-7-security-considerations"></a><span data-ttu-id="f9ff3-p203">И-7. Вопросы безопасности</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p203">I-7. Security Considerations</span></span>

<span data-ttu-id="f9ff3-p204">В системах с зарегистрированными обработчиками, которые распознают URI ms-infopath, переход по ссылке на URI ms-infopath приводит к запуску зарегистрированного приложения и попытке открыть документ по указанному URI. Приложения, регистрируемые для обработки URI ms-infopath, должны реализовать средства защиты от открытия документов из недоверенных удаленных систем, которые могут содержать вредоносный код.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p204">On systems that have registered handlers to recognize and act on ms-infopath URIs, clicking on a link to an ms-infopath URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-infopath URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="i-8-references"></a><span data-ttu-id="f9ff3-p205">И-8. Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="f9ff3-p205">I-8. References</span></span>

<span data-ttu-id="f9ff3-482">RFC 3987  интернационализированные идентификаторы ресурса (IRI)</span><span class="sxs-lookup"><span data-stu-id="f9ff3-482">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  

