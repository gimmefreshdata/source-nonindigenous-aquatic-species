node {
    stage 'configure'
        def archiveUrl = 'http://opendata.eol.org/dataset/69e3cb33-44ad-4477-be77-1d760c959e20/resource/3213ad0c-f330-4724-9210-3fbec3be330a/download/usgsnonindigenousaquaticspecies.zip'

    stage 'import'
        sh "wget --quiet https://raw.githubusercontent.com/gimmefreshdata/archive-importer/master/archives.groovy -O archives.groovy"
        archives = load 'archives.groovy'
        archives.importIfChanged(archiveUrl)
}
