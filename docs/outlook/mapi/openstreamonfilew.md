---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7e67d84320b57fe6e510b70a68088f289ef6030d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406026"
---
# <a name="openstreamonfilew"></a>OpenStreamOnFileW

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выделяет и инициализирует объект OLE **IStream** для доступа к содержимому файла. Эта функция принимает строки ЮНИКОДА в качестве аргументов, в отличие от версии ANSI этой функции [OpenStreamOnFile,](openstreamonfile.md)и, таким образом, позволяет использовать произвольные символы в имени файла, включая путь и расширение файла.
  
|||
|:-----|:-----|
|Экспортируется с помощью:  <br/> |olmapi32.dll  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFileW(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPWSTR lpszFileName,
  LPWSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Параметры

 _lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, используемых для управления созданием или открытием файла для доступа через объект OLE **IStream.** Можно установить следующие флаги: 
    
SOF_UNIQUEFILENAME
  
> Для объекта IStream необходимо создать **временный** файл. Если этот флаг установлен, также STGM_CREATE и STGM_READWRITE флаги. 
    
STGM_CREATE
  
> Файл создается, даже если он уже существует. Если параметр  _lpszFileName_ не задан, необходимо установить и этот STGM_DELETEONRELEASE, и флаг. Если STGM_CREATE установлен, необходимо также STGM_READWRITE флага. 
    
STGM_DELETEONRELEASE
  
> Файл удаляется при удалении **объекта IStream.** Если параметр  _lpszFileName_ не задан, необходимо установить и этот STGM_CREATE, и флаг. 
    
STGM_READ
  
> Файл необходимо создать или открыть с доступом только для чтения.
    
STGM_READWRITE
  
> Файл необходимо создать или открыть с разрешением на чтение и записи. Если этот флаг не установлен, STGM_CREATE не должен быть установлен.
    
 _lpszFileName_
  
> [in] Имя файла, включая путь и расширение, именуемого файла Юникода, для которого **OpenStreamOnFileW** инициализирует **объект IStream.** Если установлен SOF_UNIQUEFILENAME,  _lpszFileName_ содержит путь к каталогу, в котором необходимо создать временный файл. Если  _lpszFileName_ имеет NULL, **OpenStreamOnFileW** получает соответствующий путь из системы, и необходимо установить STGM_CREATE и STGM_DELETEONRELEASE флаги. 
    
 _lpszPrefix_
  
> [in] Префикс имени файла Юникод, по которому **OpenStreamOnFileW** инициализирует **объект IStream.** Если этот префикс установлен, он должен содержать не более трех символов. Если  _lpszPrefix_ имеет NULL, используется префикс SOF. 
    
 _lppStream_
  
> [out] Указатель на указатель на объект, который выдает интерфейс **IStream.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_ACCESS
  
> Не удалось получить доступ к файлу из-за недостаточного количества разрешений пользователя или из-за невозможность изменения файлов, доступных только для чтения.
    
MAPI_E_NOT_FOUND
  
> Указанный файл не существует.
    
## <a name="remarks"></a>Примечания

Функция **OpenStreamOnFileW** имеет два важных использования в дополнение к обработке файла с именем Юникод, различается по параметру флага SOF_UNIQUEFILENAME. Если этот флаг не установлен, **OpenStreamOnFileW** открывает объект **IStream** в существующем файле, например для копирования его содержимого в свойство **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)вложения с помощью метода **IStream::CopyTo.** В этом случае  _параметр lpszFileName_ указывает путь и имя файла. 
  
Когда SOF_UNIQUEFILENAME, **OpenStreamOnFileW** создает временный файл для хранения данных для **объекта IStream.** Для этого использования параметр  _lpszFileName_ при желании может указать путь к каталогу, в котором будет создан файл, а параметр  _lpszPrefix_ при желании может указать префикс для имени файла. 
  
После завершения вызова клиентского приложения или поставщика службы с объектом **IStream** он должен освободить его, вызывая метод OLE **IStream::Release.** 
  
MAPI использует функции, на которые указывают  _lpAllocateBuffer_ и  _lpFreeBuffer,_ для выделения большей части памяти и распределения, в частности для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Флаг SOF_UNIQUEFILENAME используется для создания временного файла с именем, уникальным для системы обмена сообщениями. Если этот флаг установлен, параметр  _lpszFileName_ задаст путь для временного файла, а параметр  _lpszPrefix_ содержит символы префикса имени файла. Сконструированы имена файлов <prefix> HHHH. TMP, где ЧЧЧ — это hexadecimal number. Если  _lpszFileName_ имеет NULL, файл будет создан во временном каталоге файлов, возвращаемом функцией Windows **GetTempPath,** или в текущем каталоге, если временный каталог файлов не назначен.
  
Если флаг SOF_UNIQUEFILENAME не установлен,  _lpszPrefix_ игнорируется, а  _lpszFileName_ должен содержать полное имя файла, который необходимо открыть или создать. Файл будет открыт или создан на основе других флагов, установленных в _ulFlags._
  
## <a name="see-also"></a>См. также



[OpenStreamOnFile](openstreamonfile.md)

