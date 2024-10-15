/_api/search/query?querytext=%27*11*%20contentclass:STS_ListItem_DocumentLibrary%20path:%22https://centralitltda.sharepoint.com/sites/GAOT-Aes2024/Documentos%20Compartilhados*%22%20path:%22https://thepoweraddicts.sharepoint.com/sites/RDTech/doc/*%22%27&RowLimit=11&STARTROW=11&selectproperties=%27Title,listitemid,Author,size,path,PictureThumbnailURL,FileExtension,ViewsLifeTime,IsDocument,ServerRedirectedEmbedURL,ServerRedirectedPreviewURL,ServerRedirectedURL,FileType,FileName,DocumentLink%27


body('Send_an_HTTP_request_to_SharePoint')?['PrimaryQueryResult']?['RelevantResults']?['Table']?['Rows']


body('Send_an_HTTP_request_to_SharePoint')?['PrimaryQueryResult']?['RelevantResults']?['TotalRows']


body('Send_an_HTTP_request_to_SharePoint')?['PrimaryQueryResult']?['RelevantResults']?['TotalRows']



Set(
    varSearchResults;
    SearchinDocuments.Run(
        Coalesce(
            txtSearch.Text;
            "*"
        );
        drpPaginationSize.Selected.Value;
        varFrom
    )
);;
Set(
    varTotalCount;
    varSearchResults.totalrows
);;
Set(
    varTotalCount;
    varSearchResults.rowcount
);;
